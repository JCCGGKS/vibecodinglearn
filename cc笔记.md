# Claude Code 配置文件笔记

## 配置文件层级结构

Claude Code 使用层级化的配置系统，优先级从高到低：

| 优先级 | 文件路径 | 作用范围 |
|--------|----------|----------|
| 1（最高）| `.claude/settings.local.json` | 项目本地（不提交到 Git） |
| 2 | `.claude/settings.json` | 项目级（可提交到 Git） |
| 3 | `~/.claude/settings.json` | 用户全局 |
| 4 | `/etc/claude-code/managed-settings.json` | 系统管理级（Linux） |

---

## 核心配置文件详解

### 1. `~/.claude/settings.json` — 用户全局配置

**路径：** `/home/fanqicheng/.claude/settings.json`

**功能：** 全局设置，对所有项目生效

**当前配置：**
```json
{
  "env": {
    "ANTHROPIC_AUTH_TOKEN": "API 认证令牌",
    "ANTHROPIC_BASE_URL": "API 基础 URL",
    "ANTHROPIC_MODEL": "默认模型"
  },
  "includeCoAuthoredBy": false
}
```

**常用配置项：**
| 配置项 | 说明 |
|--------|------|
| `env` | 环境变量（API Key、Base URL、模型等） |
| `permissions` | 权限规则（allow/ask/deny） |
| `includeCoAuthoredBy` | 是否包含共同作者信息 |
| `hooks` | 自定义钩子脚本 |
| `mcpServers` | MCP 服务器配置 |

---

### 2. `~/.claude.json` — 用户状态与项目记录

**路径：** `/home/fanqicheng/.claude.json`

**功能：** 存储用户状态、项目历史、使用统计

**主要内容：**
- `numStartups` — 启动次数
- `userID` — 用户 ID
- `projects` — 项目列表及使用统计
- `skillUsage` — 技能使用记录
- `githubRepoPaths` — GitHub 仓库映射

---

### 3. `CLAUDE.md` — 项目说明文档

**位置：** 项目根目录

**功能：** 为 Claude 提供项目上下文说明

**示例：** `/home/fanqicheng/vibecoding/CLAUDE.md`
```markdown
# CLAUDE.md

This file provides guidance to Claude Code when working with code in this repository.

## Project Overview
项目概述...

## Files
文件说明...
```

**用途：**
- 描述项目结构和目的
- 提供编码规范和约定
- 指导 Claude 如何处理项目

---

### 4. `.claude/settings.json` — 项目级配置

**位置：** 项目根目录 `.claude/settings.json`

**功能：** 项目特定设置，可提交到 Git 共享给团队

**常用配置：**
```json
{
  "permissions": {
    "allow": ["Read(**)"],
    "deny": ["Read(.env)"]
  },
  "mcpServers": {
    "server-name": {
      "command": "...",
      "args": [...]
    }
  }
}
```

---

### 5. `.claude/settings.local.json` — 项目本地配置

**位置：** 项目根目录 `.claude/settings.local.json`

**功能：** 本地覆盖设置，**不提交到 Git**

**特点：**
- 自动创建（当用户通过交互式授权时）
- 用于存储一次性权限
- 优先级高于项目级配置

---

### 6. `~/.claude/projects/` — 项目会话数据

**路径：** `/home/fanqicheng/.claude/projects/`

**功能：** 存储每个项目的历史会话和内存

**结构：**
```
~/.claude/projects/
├── -home-fanqicheng-vibecoding/
│   └── *.jsonl          # 会话记录
└── -home-fanqicheng-obsidian-local-knowledge/
    ├── *.jsonl          # 会话记录
    └── memory/          # 项目内存
```

---

### 7. `~/.claude/credentials.json` — 凭证存储

**路径：** `~/.claude/credentials.json`（Linux）

**功能：** 存储敏感凭证（API Key 等）

**注意：** 不要提交到 Git！

---

## CLAUDE.md 文件详解

### 用途
- 提供项目背景和上下文
- 定义编码风格和规范
- 指导 AI 如何处理代码

### 最佳实践
1. **项目概述**：简要描述项目目的
2. **技术栈**：列出使用的技术
3. **文件结构**：说明重要文件和目录
4. **编码规范**：代码风格要求
5. **特殊说明**：需要注意的事项

---

## 配置文件合并规则

- **数组类型**：合并所有层级的配置（不覆盖）
- **对象类型**：深层合并
- **权限规则**：按优先级应用

---

## 常用命令

```bash
# 查看当前配置
claude config

# 初始化项目 CLAUDE.md
claude /init

# 查看项目状态
claude status
```

---

## 注意事项

1. **敏感信息**：`settings.local.json` 和 `credentials.json` 不要提交到 Git
2. **权限规则**：`deny` 规则可能被忽略，需谨慎处理敏感文件
3. **配置优先级**：本地 > 项目 > 用户 > 系统
4. **MCP 服务器**：可配置在 `~/.claude.json` 或 `.mcp.json` 中

---

---

## Harness 概念

### 什么是 Harness？

**Harness = 工具 + 上下文管理 + 执行环境 + 权限控制**

它把模型的智力转化为行动力。类似于：
- 马具控制马匹 → Harness 控制 agent
- 测试框架 → 让代码在受控环境中运行

### Harness vs Scaffolding

学术界定义（arXiv 2603.05344）：以"首次prompt"为分界线
- **Scaffolding**（之前）：搭脚手架，准备工作
- **Harness**（之后）：操控，实际执行

### 核心要点

1. **Agentic Loop 是心脏**：推理 → 工具调用 → 结果回注 → 继续推理
2. **20+ 内置工具**：覆盖5个原子操作（读、写、执行、联网、编排）
3. **上下文管理**：自动压缩 + CLAUDE.md 重注入
4. **2026年是 Harness 之年**：同一模型在不同 Harness 差距 > 不同模型在同一 Harness 差距

---

## Agentic Loop（核心循环）

```
① 接收输入
   用户prompt + 系统prompt + 工具定义 + 对话历史
        ↓
② 模型推理
   Claude分析上下文，生成回复
   回复 = 文本 + 工具调用请求（可选）
        ↓
   有无工具调用？
    ├── 无 → ⑤ 返回最终结果
    └── 是 → ③ 执行工具
              Harness执行工具，收集结果
              （权限检查→执行→返回结果）
                   ↓
              ④ 结果回注
              工具结果追加到对话历史
                   ↓
              回到②，继续推理
```

---

## Claude Code 架构

```
用户（你）
    ↓ 输入Prompt/审批权限
    ↓
┌─────────────────────────────────┐
│      Harness（Claude Code）      │
├─────────────────────────────────┤
│ 工具系统          │ 权限控制           │
│ Read/Write/Edit/Bash  │ allow/deny/ask     │
│ /Grep/Glob/Agent...   │ allow/deny/ask     │
├─────────────────────────────────┤
│ 上下文管理                       │
├─────────────────────────────────┤
│ Hooks           │ Sessions          │
│ 事件钩子         │ 会话持久化         │
├─────────────────────────────────┤
│        Agentic Loop             │
│         核心循环                 │
│          API调用                │
└─────────────────────────────────┘
    ↓
Claude模型（Anthropic API）
纯文本生成 + 工具调用决策
```

---

## Harness 学习资料

### Tier 1：AI实验室一手资料

| 来源 | 内容 |
|------|------|
| Anthropic | Effective Harnesses for Long-Running Agents |
| Anthropic | Building Effective Agents（2024.12，Workflow vs Agent） |
| Anthropic | Claude Agent SDK（暴露 Agent Loop） |
| OpenAI | Harness Engineering（2026.2，~1500自动化PR） |
| OpenAI | Codex Agent Loop 详解 |

### Tier 2：学术论文

- **Building Effective AI Coding Agents**（arXiv 2603.05344）
  - Scaffolding vs Harness 边界定义

### Tier 3：行业高影响力文章

| 作者 | 文章 | 核心观点 |
|------|------|----------|
| Simon Willison | How Coding Agents Work | Coding agent = harness for LLM |
| Inngest | Your Agent Needs a Harness | Harness vs Framework 区分 |
| Swyx/Latent Space | Is Harness Engineering Real? | 竞争优势在 Harness 而非 Model |
| LangChain | Deep Agents | 开源 Harness 实现 |
| Lilian Weng | LLM Powered Autonomous Agents | 2023奠基综述 |
| Parallel.ai | What is an Agent Harness | Harness 6大组件 |

---

## 参考链接

- [Claude Code 官方文档](https://code.claude.com/docs)
- [配置文件存储位置](https://inventivehq.com/knowledge-base/claude/where-configuration-files-are-stored)

---

---

## 自定义命令（Custom Commands）

### 什么是自定义命令？

把高频重复的提示词模板固化成可复用入口，用 `/command` 快速调用。

### 命令文件位置

| 级别 | 位置 | 调用方式 |
|------|------|----------|
| 项目级 | `.claude/commands/` | `/<name>` 或 `/<dir>:<name>` |
| 个人级 | `~/.claude/commands/` | 同上 |

**例如：** `.claude/commands/frontend/component.md` → `/frontend:component`

### 命令语法

命令文件是 Markdown，用 `$ARGUMENTS` 接收参数：

```markdown
---
description: 修复 GitHub Issue
argument-hint: "[issue-number]"
---

请修复以下 GitHub Issue：

$ARGUMENTS

步骤：
1. 分析 Issue
2. 确定根因
3. 实现修复
```

### Front matter 字段

| 字段 | 作用 |
|------|------|
| `description` | 命令列表中显示的说明 |
| `argument-hint` | 自动补全时提示预期参数 |
| `disable-model-invocation` | 设为 true 后，Claude 不会自动触发 |
| `allowed-tools` | 限制命令能用的工具（安全用） |

### 变量

- `$ARGUMENTS` — 整段参数（最常用）
- `$1`、`$2`、`$3` — 按空格拆分的参数

### 实用示例

| 命令 | 用途 |
|------|------|
| `/ticket` | 工单驱动：读需求→建分支→实现→更新→建 PR |
| `/pr-review` | 审查 PR 并留评 |
| `/pr-summary` | 生成 PR 描述模板 |
| `/docs-sync` | 检查文档与代码是否一致 |
| `/code-quality` | 跑 lint/typecheck |

### 与 Skills 的关系

- 自定义命令已与 Skills 打通：`.claude/commands/review.md` 与 `.claude/skills/review/SKILL.md` 效果等价
- 推荐使用 **Skills**：支持文件目录、调用控制、子代理隔离执行

### 最佳实践

1. 保持专注 — 每个命令只做一件事
2. 清晰指令 — 提供明确的步骤
3. 善用参数 — 通过 `$ARGUMENTS` 保持灵活
4. 合理命名 — 用描述性的文件名
5. 最小权限 — 用 `allowed-tools` 限制能力

### 调用方式

```bash
/project:fix-github-issue #123   # 项目级命令
/debug 应用启动 ECONNREFUSED      # 全局命令
```

### 团队共享

将 `.claude/commands/` 提交到 Git：

```bash
git add .claude/commands/
git commit -m "Add Claude Code custom commands"
```

---

> 来源：https://claudecn.com/docs/claude-code/advanced/custom-commands/
