# Claude Certified Architect – Foundations Certification Exam Guide

> Claude认证架构师 – 基础认证考试指南

***

官方链接：

## 1. Introduction

The Claude Certified Architect – Foundations certification validates that practitioners can make informed decisions about tradeoffs when implementing real-world solutions with Claude.

> Claude认证架构师 – 基础认证验证从业者在使用Claude实施真实解决方案时做出权衡决策的能力。

This exam tests foundational knowledge across Claude Code, the Claude Agent SDK, the Claude API, and Model Context Protocol (MCP) — the core technologies used to build production-grade applications with Claude.

> 本考试测试Claude Code、Claude Agent SDK、Claude API和模型上下文协议（MCP）的基础知识——这些是使用Claude构建生产级应用的核心技术。

Questions on this exam are grounded in realistic scenarios drawn from actual customer use cases, including building agentic systems for customer support, designing multi-agent research pipelines, integrating Claude Code into CI/CD workflows, building developer productivity tools, and extracting structured data from unstructured documents.

> 本考试的题目基于实际客户使用场景，包括为客户支持构建代理系统、设计多代理研究管道、将Claude Code集成到CI/CD工作流、构建开发者生产力工具，以及从非结构化文档中提取结构化数据。

Candidates must demonstrate not only conceptual knowledge but practical judgment about architecture, configuration, and tradeoffs in production deployments.

> 候选人不仅要展示概念知识，还要展示关于架构、配置和生产环境中权衡的实践判断。

This guide describes the exam content, lists the domains and task statements tested, provides sample questions, and recommends preparation strategies. Use it alongside hands-on experience to prepare effectively.

> 本指南描述考试内容，列出测试的领域和任务陈述，提供样题，并推荐准备策略。结合实践经验使用以有效准备。

## 2. Target Candidate Description

The ideal candidate for this certification is a solution architect who designs and implements production applications with Claude. This candidate has hands-on experience with:

> 本认证的理想候选人是设计和实施Claude生产应用的解决方案架构师。

- Building agentic applications using the Claude Agent SDK, including multi-agent orchestration, subagent delegation, tool integration, and lifecycle hooks
- Configuring and customizing Claude Code for team workflows using CLAUDE.md files, Agent Skills, MCP server integrations, and plan mode
- Designing Model Context Protocol (MCP) tool and resource interfaces for backend system integration
- Engineering prompts that produce reliable structured output, leveraging JSON schemas, few-shot examples, and extraction patterns
- Managing context windows effectively across long documents, multi-turn conversations, and multi-agent handoffs
- Integrating Claude into CI/CD pipelines for automated code review, test generation, and pull request feedback
- Making sound escalation and reliability decisions, including error handling, human-in-the-loop workflows, and self-evaluation patterns

The candidate typically has 6+ months of practical experience building with Claude APIs, Agent SDK, Claude Code, and MCP, understanding both the capabilities and limitations of large language models in production environments.

> 候选人通常有6个月以上使用Claude API、Agent SDK、Claude Code和MCP构建项目的实践经验，了解大型语言模型在生产环境中的能力和局限性。

## 3. Exam Content

### Response Types

All questions on the exam are multiple choice format. Each question has one correct response and three incorrect responses (distractors).

> 所有考题均为选择题格式。每道题有一个正确答案和三个错误选项（干扰项）。

Select the single response that best completes the statement or answers the question.

> 选择最能完成陈述或回答问题的单个答案。

Distractors are response options that a candidate with incomplete knowledge or experience might choose.

> 干扰项是知识或经验不完整的候选人可能选择的选项。

Unanswered questions are scored as incorrect; there is no penalty for guessing.

> 未作答的题目计为错误；猜题没有惩罚。

### Exam Results

The exam has a pass or fail designation. The exam is scored against a minimum standard established by subject matter experts.

> 考试结果为通过或未通过。考试根据主题专家设定的最低标准进行评分。

Your results are reported as a scaled score of 100–1,000. The minimum passing score is 720.

> 成绩报告为100-1000分的比例分数。最低通过分数为720分。

Scaled scoring models help equate scores across multiple exam forms that might have slightly different difficulty levels.

> 比例评分模型有助于平衡可能具有不同难度级别的多个考试形式的分数。

***

## 4. Exam Content Outline

This exam guide includes weightings, content domains, and task statements for the exam.

> 本考试指南包括权重、内容域和任务陈述。

The exam has the following content domains and weightings:

> 考试有以下内容域和权重：

- Domain 1: Agentic Architecture & Orchestration (27% of scored content)
- Domain 2: Tool Design & MCP Integration (18% of scored content)
- Domain 3: Claude Code Configuration & Workflows (20% of scored content)
- Domain 4: Prompt Engineering & Structured Output (20% of scored content)
- Domain 5: Context Management & Reliability (15% of scored content)

### Exam Scenarios

The exam uses scenario-based questions. Each scenario presents a realistic production context that frames a set of questions. During the exam, 4 scenarios will be presented and picked at random from the full set of the 6 scenarios below.

> 考试使用基于场景的题目。每个场景呈现一个现实的生产环境来构建一组题目。考试中将从以下6个场景中随机抽取4个场景进行展示。

#### Scenario 1: Customer Support Resolution Agent

You are building a customer support resolution agent using the Claude Agent SDK. The agent handles high-ambiguity requests like returns, billing disputes, and account issues. It has access to your backend systems through custom Model Context Protocol (MCP) tools (get_customer, lookup_order, process_refund, escalate_to_human). Your target is 80%+ first-contact resolution while knowing when to escalate.

> 你正在使用Claude Agent SDK构建客户支持解决代理。该代理处理高模糊性请求，如退货、账单争议和账户问题。它可以通过自定义模型上下文协议（MCP）工具（get_customer、lookup_order、process_refund、escalate_to_human）访问你的后端系统。你的目标是实现80%以上的一次性解决率，同时知道何时升级。

Primary domains: Agentic Architecture & Orchestration, Tool Design & MCP Integration, Context Management & Reliability

> 主要领域：代理架构与编排、工具设计与MCP集成、上下文管理与可靠性

#### Scenario 2: Code Generation with Claude Code

You are using Claude Code to accelerate software development. Your team uses it for code generation, refactoring, debugging, and documentation. You need to integrate it into your development workflow with custom slash commands, CLAUDE.md configurations, and understand when to use plan mode vs direct execution.

> 你正在使用Claude Code加速软件开发。你的团队将其用于代码生成、重构、调试和文档。你需要通过自定义斜杠命令、CLAUDE.md配置将其集成到开发工作流中，并了解何时使用计划模式与直接执行。

Primary domains: Claude Code Configuration & Workflows, Context Management & Reliability

> 主要领域：Claude Code配置与工作流、上下文管理与可靠性

#### Scenario 3: Multi-Agent Research System

You are building a multi-agent research system using the Claude Agent SDK. A coordinator agent delegates to specialized subagents: one searches the web, one analyzes documents, one synthesizes findings, and one generates reports. The system researches topics and produces comprehensive, cited reports.

> 你正在使用Claude Agent SDK构建多代理研究系统。协调器代理委托给专门的子代理：一个搜索网络，一个分析文档，一个综合发现，一个生成报告。该系统研究主题并产生全面的引用报告。

Primary domains: Agentic Architecture & Orchestration, Tool Design & MCP Integration, Context Management & Reliability

> 主要领域：代理架构与编排、工具设计与MCP集成、上下文管理与可靠性

#### Scenario 4: Developer Productivity with Claude

You are building developer productivity tools using the Claude Agent SDK. The agent helps engineers explore unfamiliar codebases, understand legacy systems, generate boilerplate code, and automate repetitive tasks. It uses the built-in tools (Read, Write, Bash, Grep, Glob) and integrates with Model Context Protocol (MCP) servers.

> 你正在使用Claude Agent SDK构建开发者生产力工具。该代理帮助工程师探索不熟悉的代码库、理解遗留系统、生成样板代码并自动化重复任务。它使用内置工具（Read、Write、Bash、Grep、Glob）并与模型上下文协议（MCP）服务器集成。

Primary domains: Tool Design & MCP Integration, Claude Code Configuration & Workflows, Agentic Architecture & Orchestration

> 主要领域：工具设计与MCP集成、Claude Code配置与工作流、代理架构与编排

#### Scenario 5: Claude Code for Continuous Integration

You are integrating Claude Code into your Continuous Integration/Continuous Deployment (CI/CD) pipeline. The system runs automated code reviews, generates test cases, and provides feedback on pull requests. You need to design prompts that provide actionable feedback and minimize false positives.

> 你正在将Claude Code集成到你的持续集成/持续部署（CI/CD）管道中。该系统运行自动代码审查、生成测试用例并提供拉取请求反馈。你需要设计能够提供可操作反馈并最大程度减少误报的提示。

Primary domains: Claude Code Configuration & Workflows, Prompt Engineering & Structured Output

> 主要领域：Claude Code配置与工作流、提示工程与结构化输出

#### Scenario 6: Structured Data Extraction

You are building a structured data extraction system using Claude. The system extracts information from unstructured documents, validates the output using JavaScript Object Notation (JSON) schemas, and maintains high accuracy. It must handle edge cases gracefully and integrate with downstream systems.

> 你正在使用Claude构建结构化数据提取系统。该系统从非结构化文档中提取信息，使用JavaScript对象表示法（JSON）模式验证输出，并保持高准确性。它必须优雅地处理边缘情况并与下游系统集成。

Primary domains: Prompt Engineering & Structured Output, Context Management & Reliability

> 主要领域：提示工程与结构化输出、上下文管理与可靠性

### Domain 1: Agentic Architecture & Orchestration

**Task Statement 1.1: Design and implement agentic loops for autonomous task execution**

> **任务陈述 1.1：设计和实施自主任务执行的代理循环**

**Knowledge of:**

> **知识要求：**

- The agentic loop lifecycle: sending requests to Claude, inspecting stop_reason ("tool_use" vs "end_turn"), executing requested tools, and returning results for the next iteration
- How tool results are appended to conversation history so the model can reason about the next action
- The distinction between model-driven decision-making (Claude reasons about which tool to call next based on context) and pre-configured decision trees or tool sequences

**Skills in:**

> **技能要求：**

- Implementing agentic loop control flow that continues when stop_reason is "tool_use" and terminates when stop_reason is "end_turn"
- Adding tool results to conversation context between iterations so the model can incorporate new information into its reasoning
- Avoiding anti-patterns such as parsing natural language signals to determine loop termination, setting arbitrary iteration caps as the primary stopping mechanism, or checking for assistant text content as a completion indicator

**Task Statement 1.2: Orchestrate multi-agent systems with coordinator-subagent patterns**

> **任务陈述 1.2：使用协调器-子代理模式编排多代理系统**

**Knowledge of:**

> **知识要求：**

- Hub-and-spoke architecture where a coordinator agent manages all inter-subagent communication, error handling, and information routing
- How subagents operate with isolated context—they do not inherit the coordinator's conversation history automatically
- The role of the coordinator in task decomposition, delegation, result aggregation, and deciding which subagents to invoke based on query complexity
- Risks of overly narrow task decomposition by the coordinator, leading to incomplete coverage of broad research topics

**Skills in:**

> **技能要求：**

- Designing coordinator agents that analyze query requirements and dynamically select which subagents to invoke rather than always routing through the full pipeline
- Partitioning research scope across subagents to minimize duplication (e.g., assigning distinct subtopics or source types to each agent)
- Implementing iterative refinement loops where the coordinator evaluates synthesis output for gaps, re-delegates to search and analysis subagents with targeted queries, and re-invokes synthesis until coverage is sufficient
- Routing all subagent communication through the coordinator for observability, consistent error handling, and controlled information flow

**Task Statement 1.3: Configure subagent invocation, context passing, and spawning**

> **任务陈述 1.3：配置子代理调用、上下文传递和生成**

**Knowledge of:**

> **知识要求：**

- The Task tool as the mechanism for spawning subagents, and the requirement that allowedTools must include "Task" for a coordinator to invoke subagents
- That subagent context must be explicitly provided in the prompt—subagents do not automatically inherit parent context or share memory between invocations
- The AgentDefinition configuration including descriptions, system prompts, and tool restrictions for each subagent type
- Fork-based session management for exploring divergent approaches from a shared analysis baseline

**Skills in:**

> **技能要求：**

- Including complete findings from prior agents directly in the subagent's prompt (e.g., passing web search results and document analysis outputs to the synthesis subagent)
- Using structured data formats to separate content from metadata (source URLs, document names, page numbers) when passing context between agents to preserve attribution
- Spawning parallel subagents by emitting multiple Task tool calls in a single coordinator response rather than across separate turns
- Designing coordinator prompts that specify research goals and quality criteria rather than step-by-step procedural instructions, to enable subagent adaptability

**Task Statement 1.4: Implement multi-step workflows with enforcement and handoff patterns**

> **任务陈述 1.4：实施带有强制和交接模式的多步骤工作流**

**Knowledge of:**

> **知识要求：**

- The difference between programmatic enforcement (hooks, prerequisite gates) and prompt-based guidance for workflow ordering
- When deterministic compliance is required (e.g., identity verification before financial operations), prompt instructions alone have a non-zero failure rate
- Structured handoff protocols for mid-process escalation that include customer details, root cause analysis, and recommended actions

**Skills in:**

> **技能要求：**

- Implementing programmatic prerequisites that block downstream tool calls until prerequisite steps have completed (e.g., blocking process_refund until get_customer has returned a verified customer ID)
- Decomposing multi-concern customer requests into distinct items, then investigating each in parallel using shared context before synthesizing a unified resolution
- Compiling structured handoff summaries (customer ID, root cause, refund amount, recommended action) when escalating to human agents who lack access to the conversation transcript

**Task Statement 1.5: Apply Agent SDK hooks for tool call interception and data normalization**

> **任务陈述 1.5：应用Agent SDK钩子进行工具调用拦截和数据规范化**

**Knowledge of:**

> **知识要求：**

- Hook patterns (e.g., PostToolUse) that intercept tool results for transformation before the model processes them
- Hook patterns that intercept outgoing tool calls to enforce compliance rules (e.g., blocking refunds above a threshold)
- The distinction between using hooks for deterministic guarantees versus relying on prompt instructions for probabilistic compliance

**Skills in:**

> **技能要求：**

- Implementing PostToolUse hooks to normalize heterogeneous data formats (Unix timestamps, ISO 8601, numeric status codes) from different MCP tools before the agent processes them
- Implementing tool call interception hooks that block policy-violating actions (e.g., refunds exceeding $500) and redirect to alternative workflows (e.g., human escalation)
- Choosing hooks over prompt-based enforcement when business rules require guaranteed compliance

**Task Statement 1.6: Design task decomposition strategies for complex workflows**

> **任务陈述 1.6：设计复杂工作流的任务分解策略**

**Knowledge of:**

> **知识要求：**

- When to use fixed sequential pipelines (prompt chaining) versus dynamic adaptive decomposition based on intermediate findings
- Prompt chaining patterns that break reviews into sequential steps (e.g., analyze each file individually, then run a cross-file integration pass)
- The value of adaptive investigation plans that generate subtasks based on what is discovered at each step

**Skills in:**

> **技能要求：**

- Selecting task decomposition patterns appropriate to the workflow: prompt chaining for predictable multi-aspect reviews, dynamic decomposition for open-ended investigation tasks
- Splitting large code reviews into per-file local analysis passes plus a separate cross-file integration pass to avoid attention dilution
- Decomposing open-ended tasks (e.g., "add comprehensive tests to a legacy codebase") by first mapping structure, identifying high-impact areas, then creating a prioritized plan that adapts as dependencies are discovered

**Task Statement 1.7: Manage session state, resumption, and forking**

> **任务陈述 1.7：管理会话状态、恢复和分支**

**Knowledge of:**

> **知识要求：**

- Named session resumption using --resume \<session-name>\ to continue a specific prior conversation
- fork_session for creating independent branches from a shared analysis baseline to explore divergent approaches
- The importance of informing the agent about changes to previously analyzed files when resuming sessions after code modifications
- Why starting a new session with a structured summary is more reliable than resuming with stale tool results

**Skills in:**

>  **技能要求：**

- Using --resume with session names to continue named investigation sessions across work sessions
- Using fork_session to create parallel exploration branches (e.g., comparing two testing strategies or refactoring approaches from a shared codebase analysis)
- Choosing between session resumption (when prior context is mostly valid) and starting fresh with injected summaries (when prior tool results are stale)
- Informing a resumed session about specific file changes for targeted re-analysis rather than requiring full re-exploration

### Domain 2: Tool Design & MCP Integration

**Task Statement 2.1: Design effective tool interfaces with clear descriptions and boundaries**

> **任务陈述 2.1：设计具有清晰描述和边界的有效工具接口**

**Knowledge of:**

> **知识要求：**

- Tool descriptions as the primary mechanism LLMs use for tool selection; minimal descriptions lead to unreliable selection among similar tools
- The importance of including input formats, example queries, edge cases, and boundary explanations in tool descriptions
- How ambiguous or overlapping tool descriptions cause misrouting (e.g., analyze_content vs analyze_document with near-identical descriptions)
- The impact of system prompt wording on tool selection: keyword-sensitive instructions can create unintended tool associations

**Skills in:**

> **技能要求：**

- Writing tool descriptions that clearly differentiate each tool's purpose, expected inputs, outputs, and when to use it versus similar alternatives
- Renaming tools and updating descriptions to eliminate functional overlap (e.g., renaming analyze_content to extract_web_results with a web-specific description)
- Splitting generic tools into purpose-specific tools with defined input/output contracts (e.g., splitting a generic analyze_document into extract_data_points, summarize_content, and verify_claim_against_source)
- Reviewing system prompts for keyword-sensitive instructions that might override well-written tool descriptions

**Task Statement 2.2: Implement structured error responses for MCP tools**

> **任务陈述 2.2：为MCP工具实施结构化错误响应**

**Knowledge of:**

> **知识要求：**

- The MCP isError flag pattern for communicating tool failures back to the agent
- The distinction between transient errors (timeouts, service unavailability), validation errors (invalid input), business errors (policy violations), and permission errors
- Why uniform error responses (generic "Operation failed") prevent the agent from making appropriate recovery decisions
- The difference between retryable and non-retryable errors, and how returning structured metadata prevents wasted retry attempts

**Skills in:**

> **技能要求：**

- Returning structured error metadata including errorCategory (transient/validation/permission), isRetryable boolean, and human-readable descriptions
- Including retriable: false flags and customer-friendly explanations for business rule violations so the agent can communicate appropriately
- Implementing local error recovery within subagents for transient failures, propagating to the coordinator only errors that cannot be resolved locally along with partial results and what was attempted
- Distinguishing between access failures (needing retry decisions) and valid empty results (representing successful queries with no matches)

**Task Statement 2.3: Distribute tools appropriately across agents and configure tool choice**

> **任务陈述 2.3：适当分配工具给代理并配置工具选择**

**Knowledge of:**

> **知识要求：**

- The principle that giving an agent access to too many tools (e.g., 18 instead of 4-5) degrades tool selection reliability by increasing decision complexity
- Why agents with tools outside their specialization tend to misuse them (e.g., a synthesis agent attempting web searches)
- Scoped tool access: giving agents only the tools needed for their role, with limited cross-role tools for specific high-frequency needs
- tool_choice configuration options: "auto", "any", and forced tool selection ({"type": "tool", "name": "..."})

**Skills in:**

> **技能要求：**

- Restricting each subagent's tool set to those relevant to its role, preventing cross-specialization misuse
- Replacing generic tools with constrained alternatives (e.g., replacing fetch_url with load_document that validates document URLs)
- Providing scoped cross-role tools for high-frequency needs (e.g., a verify_fact tool for the synthesis agent) while routing complex cases through the coordinator
- Using tool_choice forced selection to ensure a specific tool is called first (e.g., forcing extract_metadata before enrichment tools), then processing subsequent steps in follow-up turns
- Setting tool_choice: "any" to guarantee the model calls a tool rather than returning conversational text

**Task Statement 2.4: Integrate MCP servers into Claude Code and agent workflows**

> **任务陈述 2.4：将MCP服务器集成到Claude Code和代理工作流**

**Knowledge of:**

> **知识要求：**

- MCP server scoping: project-level (.mcp.json) for shared team tooling vs user-level (~/.claude.json) for personal/experimental servers
- Environment variable expansion in .mcp.json (e.g., ${GITHUB_TOKEN}) for credential management without committing secrets
- That tools from all configured MCP servers are discovered at connection time and available simultaneously to the agent
- MCP resources as a mechanism for exposing content catalogs (e.g., issue summaries, documentation hierarchies, database schemas) to reduce exploratory tool calls

**Skills in:**

> **技能要求：**

- Configuring shared MCP servers in project-scoped .mcp.json with environment variable expansion for authentication tokens
- Configuring personal/experimental MCP servers in user-scoped ~/.claude.json
- Enhancing MCP tool descriptions to explain capabilities and outputs in detail, preventing the agent from preferring built-in tools (like Grep) over more capable MCP tools
- Choosing existing community MCP servers over custom implementations for standard integrations (e.g., Jira), reserving custom servers for team-specific workflows
- Exposing content catalogs as MCP resources to give agents visibility into available data without requiring exploratory tool calls

**Task Statement 2.5: Select and apply built-in tools (Read, Write, Edit, Bash, Grep, Glob) effectively**

> **任务陈述 2.5：有效选择和应用内置工具（Read、Write、Edit、Bash、Grep、Glob）**

**Knowledge of:**

> **知识要求：**

- Grep for content search (searching file contents for patterns like function names, error messages, or import statements)
- Glob for file path pattern matching (finding files by name or extension patterns)
- Read/Write for full file operations; Edit for targeted modifications using unique text matching
- When Edit fails due to non-unique text matches, using Read + Write as a fallback for reliable file modifications

**Skills in:**

> **技能要求：**

- Selecting Grep for searching code content across a codebase (e.g., finding all callers of a function, locating error messages)
- Selecting Glob for finding files matching naming patterns (e.g., **/*.test.tsx)
- Using Read to load full file contents followed by Write when Edit cannot find unique anchor text
- Building codebase understanding incrementally: starting with Grep to find entry points, then using Read to follow imports and trace flows, rather than reading all files upfront
- Tracing function usage across wrapper modules by first identifying all exported names, then searching for each name across the codebase

### Domain 3: Claude Code Configuration & Workflows

**Task Statement 3.1: Configure CLAUDE.md files with appropriate hierarchy, scoping, and modular organization**

> **任务陈述 3.1：使用适当的层次结构、作用域和模块化组织配置CLAUDE.md文件**

**Knowledge of:**

> **知识要求：**

- The CLAUDE.md configuration hierarchy: user-level (~/.claude/CLAUDE.md), project-level (.claude/CLAUDE.md or root CLAUDE.md), and directory-level (subdirectory CLAUDE.md files)
- That user-level settings apply only to that user—instructions in ~/.claude/CLAUDE.md are not shared with teammates via version control
- The @import syntax for referencing external files to keep CLAUDE.md modular (e.g., importing specific standards files relevant to each package)
- .claude/rules/ directory for organizing topic-specific rule files as an alternative to a monolithic CLAUDE.md

**Skills in:**

> **技能要求：**

- Diagnosing configuration hierarchy issues (e.g., a new team member not receiving instructions because they're in user-level rather than project-level configuration)
- Using @import to selectively include relevant standards files in each package's CLAUDE.md based on maintainer domain knowledge
- Splitting large CLAUDE.md files into focused topic-specific files in .claude/rules/ (e.g., testing.md, api-conventions.md, deployment.md)
- Using the /memory command to verify which memory files are loaded and diagnose inconsistent behavior across sessions

**Task Statement 3.2: Create and configure custom slash commands and skills**

> **任务陈述 3.2：创建和配置自定义斜杠命令和技能**

**Knowledge of:**

> **知识要求：**

- Project-scoped commands in .claude/commands/ (shared via version control) vs user-scoped commands in ~/.claude/commands/ (personal)
- Skills in .claude/skills/ with SKILL.md files that support frontmatter configuration including context: fork, allowed-tools, and argument-hint
- The context: fork frontmatter option for running skills in an isolated sub-agent context, preventing skill outputs from polluting the main conversation
- Personal skill customization: creating personal variants in ~/.claude/skills/ with different names to avoid affecting teammates

**Skills in:**

> **技能要求：**

- Creating project-scoped slash commands in .claude/commands/ for team-wide availability via version control
- Using context: fork to isolate skills that produce verbose output (e.g., codebase analysis) or exploratory context (e.g., brainstorming alternatives) from the main session
- Configuring allowed-tools in skill frontmatter to restrict tool access during skill execution (e.g., limiting to file write operations to prevent destructive actions)
- Using argument-hint frontmatter to prompt developers for required parameters when they invoke the skill without arguments
- Choosing between skills (on-demand invocation for task-specific workflows) and CLAUDE.md (always-loaded universal standards)

**Task Statement 3.3: Apply path-specific rules for conditional convention loading**

> **任务陈述 3.3：应用路径特定规则进行条件约定加载**

**Knowledge of:**

> **知识要求：**

- .claude/rules/ files with YAML frontmatter paths fields containing glob patterns for conditional rule activation
- How path-scoped rules load only when editing matching files, reducing irrelevant context and token usage
- The advantage of glob-pattern rules over directory-level CLAUDE.md files for conventions that span multiple directories (e.g., test files spread throughout a codebase)

**Skills in:**

> **技能要求：**

- Creating .claude/rules/ files with YAML frontmatter path scoping (e.g., paths: ["terraform/**/*"]) so rules load only when editing matching files
- Using glob patterns in path-specific rules to apply conventions to files by type regardless of directory location (e.g., **/*.test.tsx for all test files)
- Choosing path-specific rules over subdirectory CLAUDE.md files when conventions must apply to files spread across the codebase

**Task Statement 3.4: Determine when to use plan mode vs direct execution**

> **任务陈述 3.4：确定何时使用计划模式与直接执行**

**Knowledge of:**

> **知识要求：**

- Plan mode is designed for complex tasks involving large-scale changes, multiple valid approaches, architectural decisions, and multi-file modifications
- Direct execution is appropriate for simple, well-scoped changes (e.g., adding a single validation check to one function)
- Plan mode enables safe codebase exploration and design before committing to changes, preventing costly rework
- The Explore subagent for isolating verbose discovery output and returning summaries to preserve main conversation context

**Skills in:**

> **技能要求：**

- Selecting plan mode for tasks with architectural implications (e.g., microservice restructuring, library migrations affecting 45+ files, choosing between integration approaches with different infrastructure requirements)
- Selecting direct execution for well-understood changes with clear scope (e.g., a single-file bug fix with a clear stack trace, adding a date validation conditional)
- Using the Explore subagent for verbose discovery phases to prevent context window exhaustion during multi-phase tasks
- Combining plan mode for investigation with direct execution for implementation (e.g., planning a library migration, then executing the planned approach)

**Task Statement 3.5: Apply iterative refinement techniques for progressive improvement**

> **任务陈述 3.5：应用迭代改进技术进行渐进式改进**

**Knowledge of:**

> **知识要求：**

- Concrete input/output examples as the most effective way to communicate expected transformations when prose descriptions are interpreted inconsistently
- Test-driven iteration: writing test suites first, then iterating by sharing test failures to guide progressive improvement
- The interview pattern: having Claude ask questions to surface considerations the developer may not have anticipated before implementing
- When to provide all issues in a single message (interacting problems) versus fixing them sequentially (independent problems)

**Skills in:**

> **技能要求：**

- Providing 2-3 concrete input/output examples to clarify transformation requirements when natural language descriptions produce inconsistent results
- Writing test suites covering expected behavior, edge cases, and performance requirements before implementation, then iterating by sharing test failures
- Using the interview pattern to surface design considerations (e.g., cache invalidation strategies, failure modes) before implementing solutions in unfamiliar domains
- Providing specific test cases with example input and expected output to fix edge case handling (e.g., null values in migration scripts)
- Addressing multiple interacting issues in a single detailed message when fixes interact, versus sequential iteration for independent issues

**Task Statement 3.6: Integrate Claude Code into CI/CD pipelines**

> **任务陈述 3.6：将Claude Code集成到CI/CD管道**

**Knowledge of:**

> **知识要求：**

- The -p (or --print) flag for running Claude Code in non-interactive mode in automated pipelines
- --output-format json and --json-schema CLI flags for enforcing structured output in CI contexts
- CLAUDE.md as the mechanism for providing project context (testing standards, fixture conventions, review criteria) to CI-invoked Claude Code
- Session context isolation: why the same Claude session that generated code is less effective at reviewing its own changes compared to an independent review instance

**Skills in:**

> **技能要求：**

- Running Claude Code in CI with the -p flag to prevent interactive input hangs
- Using --output-format json with --json-schema to produce machine-parseable structured findings for automated posting as inline PR comments
- Including prior review findings in context when re-running reviews after new commits, instructing Claude to report only new or still-unaddressed issues to avoid duplicate comments
- Providing existing test files in context so test generation avoids suggesting duplicate scenarios already covered by the test suite
- Documenting testing standards, valuable test criteria, and available fixtures in CLAUDE.md to improve test generation quality and reduce low-value test output

### Domain 4: Prompt Engineering & Structured Output

**Task Statement 4.1: Design prompts with explicit criteria to improve precision and reduce false positives**

> **任务陈述 4.1：设计具有明确标准的提示以提高精度并减少误报**

**Knowledge of:**

> **知识要求：**

- The importance of explicit criteria over vague instructions (e.g., "flag comments only when claimed behavior contradicts actual code behavior" vs "check that comments are accurate")
- How general instructions like "be conservative" or "only report high-confidence findings" fail to improve precision compared to specific categorical criteria
- The impact of false positive rates on developer trust: high false positive categories undermine confidence in accurate categories

**Skills in:**

> **技能要求：**

- Writing specific review criteria that define which issues to report (bugs, security) versus skip (minor style, local patterns) rather than relying on confidence-based filtering
- Temporarily disabling high false-positive categories to restore developer trust while improving prompts for those categories
- Defining explicit severity criteria with concrete code examples for each severity level to achieve consistent classification

**Task Statement 4.2: Apply few-shot prompting to improve output consistency and quality**

> **任务陈述 4.2：应用少样本提示以提高输出一致性和质量**

**Knowledge of:**

> **知识要求：**

- Few-shot examples as the most effective technique for achieving consistently formatted, actionable output when detailed instructions alone produce inconsistent results
- The role of few-shot examples in demonstrating ambiguous-case handling (e.g., tool selection for ambiguous requests, branch-level test coverage gaps)
- How few-shot examples enable the model to generalize judgment to novel patterns rather than matching only pre-specified cases
- The effectiveness of few-shot examples for reducing hallucination in extraction tasks (e.g., handling informal measurements, varied document structures)

**Skills in:**

> **技能要求：**

- Creating 2-4 targeted few-shot examples for ambiguous scenarios that show reasoning for why one action was chosen over plausible alternatives
- Including few-shot examples that demonstrate specific desired output format (location, issue, severity, suggested fix) to achieve consistency
- Providing few-shot examples distinguishing acceptable code patterns from genuine issues to reduce false positives while enabling generalization
- Using few-shot examples to demonstrate correct handling of varied document structures (inline citations vs bibliographies, methodology sections vs embedded details)
- Adding few-shot examples showing correct extraction from documents with varied formats to address empty/null extraction of required fields

**Task Statement 4.3: Enforce structured output using tool use and JSON schemas**

> **任务陈述 4.3：使用工具使用和JSON模式强制结构化输出**

**Knowledge of:**

> **知识要求：**

- Tool use (tool_use) with JSON schemas as the most reliable approach for guaranteed schema-compliant structured output, eliminating JSON syntax errors
- The distinction between tool_choice: "auto" (model may return text instead of calling a tool), "any" (model must call a tool but can choose which), and forced tool selection (model must call a specific named tool)
- That strict JSON schemas via tool use eliminate syntax errors but do not prevent semantic errors (e.g., line items that don't sum to total, values in wrong fields)
- Schema design considerations: required vs optional fields, enum fields with "other" + detail string patterns for extensible categories

**Skills in:**

> **技能要求：**

- Defining extraction tools with JSON schemas as input parameters and extracting structured data from the tool_use response
- Setting tool_choice: "any" to guarantee structured output when multiple extraction schemas exist and the document type is unknown
- Forcing a specific tool with tool_choice: {"type": "tool", "name": "extract_metadata"} to ensure a particular extraction runs before enrichment steps
- Designing schema fields as optional (nullable) when source documents may not contain the information, preventing the model from fabricating values to satisfy required fields
- Adding enum values like "unclear" for ambiguous cases and "other" + detail fields for extensible categorization
- Including format normalization rules in prompts alongside strict output schemas to handle inconsistent source formatting

**Task Statement 4.4: Implement validation, retry, and feedback loops for extraction quality**

> **任务陈述 4.4：实施验证、重试和反馈循环以确保提取质量**

**Knowledge of:**

> **知识要求：**

- Retry-with-error-feedback: appending specific validation errors to the prompt on retry to guide the model toward correction
- The limits of retry: retries are ineffective when the required information is simply absent from the source document (vs format or structural errors)
- Feedback loop design: tracking which code constructs trigger findings (detected_pattern field) to enable systematic analysis of dismissal patterns
- The difference between semantic validation errors (values don't sum, wrong field placement) and schema syntax errors (eliminated by tool use)

**Skills in:**

> **技能要求：**

- Implementing follow-up requests that include the original document, the failed extraction, and specific validation errors for model self-correction
- Identifying when retries will be ineffective (e.g., information exists only in an external document not provided) versus when they will succeed (format mismatches, structural output errors)
- Adding detected_pattern fields to structured findings to enable analysis of false positive patterns when developers dismiss findings
- Designing self-correction validation flows: extracting "calculated_total" alongside "stated_total" to flag discrepancies, adding "conflict_detected" booleans for inconsistent source data

**Task Statement 4.5: Design efficient batch processing strategies**

> **任务陈述 4.5：设计高效的批处理策略**

**Knowledge of:**

> **知识要求：**

- The Message Batches API: 50% cost savings, up to 24-hour processing window, no guaranteed latency SLA
- Batch processing is appropriate for non-blocking, latency-tolerant workloads (overnight reports, weekly audits, nightly test generation) and inappropriate for blocking workflows (pre-merge checks)
- The batch API does not support multi-turn tool calling within a single request (cannot execute tools mid-request and return results)
- custom_id fields for correlating batch request/response pairs

**Skills in:**

> **技能要求：**

- Matching API approach to workflow latency requirements: synchronous API for blocking pre-merge checks, batch API for overnight/weekly analysis
- Calculating batch submission frequency based on SLA constraints (e.g., 4-hour windows to guarantee 30-hour SLA with 24-hour batch processing)
- Handling batch failures: resubmitting only failed documents (identified by custom_id) with appropriate modifications (e.g., chunking documents that exceeded context limits)
- Using prompt refinement on a sample set before batch-processing large volumes to maximize first-pass success rates and reduce iterative resubmission costs

**Task Statement 4.6: Design multi-instance and multi-pass review architectures**

> **任务陈述 4.6：设计多实例和多轮审查架构**

**Knowledge of:**

> **知识要求：**

- Self-review limitations: a model retains reasoning context from generation, making it less likely to question its own decisions in the same session
- Independent review instances (without prior reasoning context) are more effective at catching subtle issues than self-review instructions or extended thinking
- Multi-pass review: splitting large reviews into per-file local analysis passes plus cross-file integration passes to avoid attention dilution and contradictory findings

**Skills in:**

> **技能要求：**

- Using a second independent Claude instance to review generated code without the generator's reasoning context
- Splitting large multi-file reviews into focused per-file passes for local issues plus separate integration passes for cross-file data flow analysis
- Running verification passes where the model self-reports confidence alongside each finding to enable calibrated review routing

### Domain 5: Context Management & Reliability

**Task Statement 5.1: Manage conversation context to preserve critical information across long interactions**

> **任务陈述 5.1：管理对话上下文以在长交互中保留关键信息**

**Knowledge of:**

> **知识要求：**

- Progressive summarization risks: condensing numerical values, percentages, dates, and customer-stated expectations into vague summaries
- The "lost in the middle" effect: models reliably process information at the beginning and end of long inputs but may omit findings from middle sections
- How tool results accumulate in context and consume tokens disproportionately to their relevance (e.g., 40+ fields per order lookup when only 5 are relevant)
- The importance of passing complete conversation history in subsequent API requests to maintain conversational coherence

**Skills in:**

> **技能要求：**

- Extracting transactional facts (amounts, dates, order numbers, statuses) into a persistent "case facts" block included in each prompt, outside summarized history
- Extracting and persisting structured issue data (order IDs, amounts, statuses) into a separate context layer for multi-issue sessions
- Trimming verbose tool outputs to only relevant fields before they accumulate in context (e.g., keeping only return-relevant fields from order lookups)
- Placing key findings summaries at the beginning of aggregated inputs and organizing detailed results with explicit section headers to mitigate position effects
- Requiring subagents to include metadata (dates, source locations, methodological context) in structured outputs to support accurate downstream synthesis
- Modifying upstream agents to return structured data (key facts, citations, relevance scores) instead of verbose content and reasoning chains when downstream agents have limited context budgets

**Task Statement 5.2: Design effective escalation and ambiguity resolution patterns**

> **任务陈述 5.2：设计有效的升级和歧义解决模式**

**Knowledge of:**

> **知识要求：**

- Appropriate escalation triggers: customer requests for a human, policy exceptions/gaps (not just complex cases), and inability to make meaningful progress
- The distinction between escalating immediately when a customer explicitly demands it versus offering to resolve when the issue is straightforward
- Why sentiment-based escalation and self-reported confidence scores are unreliable proxies for actual case complexity
- How multiple customer matches require clarification (requesting additional identifiers) rather than heuristic selection

**Skills in:**

> **技能要求：**

- Adding explicit escalation criteria with few-shot examples to the system prompt demonstrating when to escalate versus resolve autonomously
- Honoring explicit customer requests for human agents immediately without first attempting investigation
- Acknowledging frustration while offering resolution when the issue is within the agent's capability, escalating only if the customer reiterates their preference
- Escalating when policy is ambiguous or silent on the customer's specific request (e.g., competitor price matching when policy only addresses own-site adjustments)
- Instructing the agent to ask for additional identifiers when tool results return multiple matches, rather than selecting based on heuristics

**Task Statement 5.3: Implement error propagation strategies across multi-agent systems**

> **任务陈述 5.3：在多代理系统中实施错误传播策略**

**Knowledge of:**

> **知识要求：**

- Structured error context (failure type, attempted query, partial results, alternative approaches) as enabling intelligent coordinator recovery decisions
- The distinction between access failures (timeouts needing retry decisions) and valid empty results (successful queries with no matches)
- Why generic error statuses ("search unavailable") hide valuable context from the coordinator
- Why silently suppressing errors (returning empty results as success) or terminating entire workflows on single failures are both anti-patterns

**Skills in:**

> **技能要求：**

- Returning structured error context including failure type, what was attempted, partial results, and potential alternatives to enable coordinator recovery
- Distinguishing access failures from valid empty results in error reporting so the coordinator can make appropriate decisions
- Having subagents implement local recovery for transient failures and only propagate errors they cannot resolve, including what was attempted and partial results
- Structuring synthesis output with coverage annotations indicating which findings are well-supported versus which topic areas have gaps due to unavailable sources

**Task Statement 5.4: Manage context effectively in large codebase exploration**

> **任务陈述 5.4：在大型代码库探索中有效管理上下文**

**Knowledge of:**

> **知识要求：**

- Context degradation in extended sessions: models start giving inconsistent answers and referencing "typical patterns" rather than specific classes discovered earlier
- The role of scratchpad files for persisting key findings across context boundaries
- Subagent delegation for isolating verbose exploration output while the main agent coordinates high-level understanding
- Structured state persistence for crash recovery: each agent exports state to a known location, and the coordinator loads a manifest on resume

**Skills in:**

> **技能要求：**

- Spawning subagents to investigate specific questions (e.g., "find all test files," "trace refund flow dependencies") while the main agent preserves high-level coordination
- Having agents maintain scratchpad files recording key findings, referencing them for subsequent questions to counteract context degradation
- Summarizing key findings from one exploration phase before spawning sub-agents for the next phase, injecting summaries into initial context
- Designing crash recovery using structured agent state exports (manifests) that the coordinator loads on resume and injects into agent prompts
- Using /compact to reduce context usage during extended exploration sessions when context fills with verbose discovery output

**Task Statement 5.5: Design human review workflows and confidence calibration**

> **任务陈述 5.5：设计人工审查工作流和置信度校准**

**Knowledge of:**

> **知识要求：**

- The risk that aggregate accuracy metrics (e.g., 97% overall) may mask poor performance on specific document types or fields
- Stratified random sampling for measuring error rates in high-confidence extractions and detecting novel error patterns
- Field-level confidence scores calibrated using labeled validation sets for routing review attention
- The importance of validating accuracy by document type and field segment before automating high-confidence extractions

**Skills in:**

> **技能要求：**

- Implementing stratified random sampling of high-confidence extractions for ongoing error rate measurement and novel pattern detection
- Analyzing accuracy by document type and field to verify consistent performance across all segments before reducing human review
- Having models output field-level confidence scores, then calibrating review thresholds using labeled validation sets
- Routing extractions with low model confidence or ambiguous/contradictory source documents to human review, prioritizing limited reviewer capacity

**Task Statement 5.6: Preserve information provenance and handle uncertainty in multi-source synthesis**

> **任务陈述 5.6：在多源综合中保留信息来源并处理不确定性**

**Knowledge of:**

> **知识要求：**

- How source attribution is lost during summarization steps when findings are compressed without preserving claim-source mappings
- The importance of structured claim-source mappings that the synthesis agent must preserve and merge when combining findings
- How to handle conflicting statistics from credible sources: annotating conflicts with source attribution rather than arbitrarily selecting one value
- Temporal data: requiring publication/collection dates in structured outputs to prevent temporal differences from being misinterpreted as contradictions

**Skills in:**

> **技能要求：**

- Requiring subagents to output structured claim-source mappings (source URLs, document names, relevant excerpts) that downstream agents preserve through synthesis
- Structuring reports with explicit sections distinguishing well-established findings from contested ones, preserving original source characterizations and methodological context
- Completing document analysis with conflicting values included and explicitly annotated, letting the coordinator decide how to reconcile before passing to synthesis
- Requiring subagents to include publication or data collection dates in structured outputs to enable correct temporal interpretation
- Rendering different content types appropriately in synthesis outputs—financial data as tables, news as prose, technical findings as structured lists—rather than converting everything to a uniform format

## 5. Sample Questions

The following sample questions illustrate the format and difficulty level of the exam. These are drawn from the practice test and include explanations to aid learning.

> 以下样题展示了考试的格式和难度级别。这些题目来自练习测试，包含解释以帮助学习。

### Scenario: Customer Support Resolution Agent

**Question 1: Production data shows that in 12% of cases, your agent skips get_customer entirely and calls lookup_order using only the customer's stated name, occasionally leading to misidentified accounts and incorrect refunds. What change would most effectively address this reliability issue?**

> 问题1：生产数据显示，在12%的情况下，你的代理完全跳过了get_customer，仅使用客户提供的姓名调用lookup_order，偶尔导致账户识别错误和退款错误。什么改变最能有效解决这个可靠性问题？

- A) Add a programmatic prerequisite that blocks lookup_order and process_refund calls until get_customer has returned a verified customer ID.
  添加一个程序化先决条件，阻止lookup_order和process_refund调用，直到get_customer返回已验证的客户ID。
- B) Enhance the system prompt to state that customer verification via get_customer is mandatory before any order operations.
  增强系统提示，说明在进行任何订单操作之前，通过get_customer进行客户验证是强制性的。
- C) Add few-shot examples showing the agent always calling get_customer first, even when customers volunteer order details.
  添加少样本示例，展示代理始终先调用get_customer，即使客户主动提供订单详情。
- D) Implement a routing classifier that analyzes each request and enables only the subset of tools appropriate for that request type.
  实现一个路由分类器，分析每个请求并仅启用适合该请求类型的工具子集。

> **Correct Answer:** A

**Explanation:** When a specific tool sequence is required for critical business logic (like verifying customer identity before processing refunds), programmatic enforcement provides deterministic guarantees that prompt-based approaches cannot. Options B and C rely on probabilistic LLM compliance, which is insufficient when errors have financial consequences. Option D addresses tool availability rather than tool ordering, which is not the actual problem.

> 解析：当关键业务逻辑需要特定的工具序列时（如处理退款前验证客户身份），程序化执行能提供基于提示的方法无法实现的确定性保证。选项B和C依赖于概率性的LLM遵从，当错误具有财务后果时这还不够。选项D解决的是工具可用性而非工具顺序，这不是实际问题所在。

**Question 2: Production logs show the agent frequently calls get_customer when users ask about orders (e.g., "check my order #12345"), instead of calling lookup_order. Both tools have minimal descriptions ("Retrieves customer information" / "Retrieves order details") and accept similar identifier formats. What's the most effective first step to improve tool selection reliability?**

> 问题2：生产日志显示，当用户询问订单时（例如"check my order #12345"），代理经常调用get_customer，而不是调用lookup_order。这两个工具的描述都很简略（"检索客户信息"/"检索订单详情"）且接受类似的标识符格式。提高工具选择可靠性的最有效第一步是什么？

- A) Add few-shot examples to the system prompt demonstrating correct tool selection patterns, with 5-8 examples showing order-related queries routing to lookup_order.
  向系统提示添加少样本示例，展示正确的工具选择模式，包含5-8个显示订单相关查询路由到lookup_order的示例。
- B) Expand each tool's description to include input formats it handles, example queries, edge cases, and boundaries explaining when to use it versus similar tools.
  扩展每个工具的描述，包含其处理的输入格式、示例查询、边界情况和解释何时使用该工具而非类似工具的边界说明。
- C) Implement a routing layer that parses user input before each turn and pre-selects the appropriate tool based on detected keywords and identifier patterns.
  实现一个路由层，在每轮交互前解析用户输入，并根据检测到的关键字和标识符模式预选适当的工具。
- D) Consolidate both tools into a single lookup_entity tool that accepts any identifier and internally determines which backend to query.
  将两个工具合并为一个lookup_entity工具，接受任何标识符并在内部决定查询哪个后端。

> **Correct Answer:** B

**Explanation:** Tool descriptions are the primary mechanism LLMs use for tool selection. When descriptions are minimal, models lack the context to differentiate between similar tools. Option B directly addresses this root cause with a low-effort, high-leverage fix. Few-shot examples (A) add token overhead without fixing the underlying issue. A routing layer (C) is over-engineered and bypasses the LLM's natural language understanding. Consolidating tools (D) is a valid architectural choice but requires more effort than a "first step" warrants when the immediate problem is inadequate descriptions.

> 解析：工具描述是LLM用于工具选择的主要机制。当描述过于简略时，模型缺乏区分类似工具的上下文。选项B直接解决了这个根本原因，是一种低投入、高杠杆的修复。少样本示例（A）增加了令牌开销但没有解决根本问题。路由层（C）过度设计，绕过了LLM的自然语言理解能力。合并工具（D）是有效的架构选择，但当即时问题是描述不充分时，这比"第一步"所需的工作量更大。

**Question 3: Your agent achieves 55% first-contact resolution, well below the 80% target. Logs show it escalates straightforward cases (standard damage replacements with photo evidence) while attempting to autonomously handle complex situations requiring policy exceptions. What's the most effective way to improve escalation calibration?**

> 问题3：你的代理实现了一次性解决率55%，远低于80%的目标。日志显示它升级了简单案例（有照片证据的标准损坏更换），却试图自主处理需要政策例外的复杂情况。提高升级校准的最有效方法是什么？

- A) Add explicit escalation criteria to your system prompt with few-shot examples demonstrating when to escalate versus resolve autonomously.
  向系统提示添加明确的升级标准，附带少样本示例展示何时升级与何时自主解决。
- B) Have the agent self-report a confidence score (1-10) before each response and automatically route requests to humans when confidence falls below a threshold.
  让代理在每次响应前自报置信度分数（1-10分），当置信度低于阈值时自动将请求路由给人工。
- C) Deploy a separate classifier model trained on historical tickets to predict which requests need escalation before the main agent begins processing.
  部署一个基于历史工单训练的分类器模型，在主代理开始处理前预测哪些请求需要升级。
- D) Implement sentiment analysis to detect customer frustration levels and automatically escalate when negative sentiment exceeds a threshold.
  实施情感分析以检测客户挫折程度，当负面情感超过阈值时自动升级。

> **Correct Answer:** A

**Explanation:** Adding explicit escalation criteria with few-shot examples directly addresses the root cause: unclear decision boundaries. This is the proportionate first response before adding infrastructure. Option B fails because LLM self-reported confidence is poorly calibrated—the agent is already incorrectly confident on hard cases. Option C is over-engineered, requiring labeled data and ML infrastructure when prompt optimization hasn't been tried. Option D solves a different problem entirely; sentiment doesn't correlate with case complexity, which is the actual issue.

> 解析：添加带有少样本示例的明确升级标准直接解决了根本原因：决策边界不清晰。这是在添加基础设施之前适度的首次响应。选项B失败是因为LLM自报置信度校准不佳——代理已经在困难案例上错误地自信。选项C过度工程化，当提示优化尚未尝试时就需要标注数据和ML基础设施。选项D完全解决了不同的问题；情感与案例复杂性不相关，而后者才是实际问题。

### Scenario: Code Generation with Claude Code

**Question 4: You want to create a custom /review slash command that runs your team's standard code review checklist. This command should be available to every developer when they clone or pull the repository. Where should you create this command file?**

> 问题4：你想创建一个自定义的/review斜杠命令，用于运行团队的代码审查清单。该命令应在每个开发者克隆或拉取仓库时可用。你应该在哪里创建这个命令文件？

- A) In the .claude/commands/ directory in the project repository
  在项目仓库的.claude/commands/目录中
- B) In ~/.claude/commands/ in each developer's home directory
  在每个开发者主目录的~/.claude/commands/中
- C) In the CLAUDE.md file at the project root
  在项目根目录的CLAUDE.md文件中
- D) In a .claude/config.json file with a commands array
  在带有commands数组的.claude/config.json文件中

> **Correct Answer:** A

**Explanation:** Project-scoped custom slash commands should be stored in the .claude/commands/ directory within the repository. These commands are version-controlled and automatically available to all developers when they clone or pull the repo. Option B (~/.claude/commands/) is for personal commands that aren't shared via version control. Option C (CLAUDE.md) is for project instructions and context, not command definitions. Option D describes a configuration mechanism that doesn't exist in Claude Code.

> 解析：项目作用域的自定义斜杠命令应存储在仓库内的.claude/commands/目录中。这些命令受版本控制，当开发者克隆或拉取仓库时自动对所有开发者可用。选项B（~/.claude/commands/）用于不通过版本控制共享的个人命令。选项C（CLAUDE.md）用于项目指令和上下文，而非命令定义。选项D描述了一种在Claude Code中不存在的配置机制。

**Question 5: You've been assigned to restructure the team's monolithic application into microservices. This will involve changes across dozens of files and requires decisions about service boundaries and module dependencies. Which approach should you take?**

> 问题5：你被指派将团队的单体应用重构为微服务。这将涉及几十个文件的更改，并需要决定服务边界和模块依赖关系。你应该采取哪种方法？

- A) Enter plan mode to explore the codebase, understand dependencies, and design an implementation approach before making changes.
  进入计划模式，探索代码库，了解依赖关系，并在进行更改前设计实现方案。
- B) Start with direct execution and make changes incrementally, letting the implementation reveal the natural service boundaries.
  从直接执行开始，逐步进行更改，让实现揭示自然的服务边界。
- C) Use direct execution with comprehensive upfront instructions detailing exactly how each service should be structured.
  使用直接执行并附带详细的前置指令，准确说明每个服务的结构。
- D) Begin in direct execution mode and only switch to plan mode if you encounter unexpected complexity during implementation.
  以直接执行模式开始，仅在实现过程中遇到意外复杂性时才切换到计划模式。

> **Correct Answer:** A

**Explanation:** Plan mode is designed for complex tasks involving large-scale changes, multiple valid approaches, and architectural decisions—exactly what monolith-to-microservices restructuring requires. It enables safe codebase exploration and design before committing to changes. Option B risks costly rework when dependencies are discovered late. Option C assumes you already know the right structure without exploring the code. Option D ignores that the complexity is already stated in the requirements, not something that might emerge later.

> 解析：计划模式专为涉及大规模更改、多种有效方法和架构决策的复杂任务而设计——这正是单体到微服务重构所需的。它能够在提交更改前安全地探索代码库并设计方案。选项B在依赖关系被较晚发现时可能导致昂贵的返工。选项C假定你已经知道正确的结构而无需探索代码。选项D忽略了复杂性已在需求中说明，而不是可能后来出现的东西。

**Question 6: Your codebase has distinct areas with different coding conventions: React components use functional style with hooks, API handlers use async/await with specific error handling, and database models follow a repository pattern. Test files are spread throughout the codebase alongside the code they test (e.g., Button.test.tsx next to Button.tsx), and you want all tests to follow the same conventions regardless of location. What's the most maintainable way to ensure Claude automatically applies the correct conventions when generating code?**

> 问题6：你的代码库有不同区域使用不同的编码约定：React组件使用带有钩子的函数式风格，API处理程序使用带有特定错误处理的async/await，数据库模型遵循仓库模式。测试文件分散在整个代码库中，与它们测试的代码放在一起（例如Button.test.tsx在Button.tsx旁边），你希望所有测试无论位置如何都遵循相同的约定。确保Claude在生成代码时自动应用正确约定的最可维护方式是什么？

- A) Create rule files in .claude/rules/ with YAML frontmatter specifying glob patterns to conditionally apply conventions based on file paths
  在.claude/rules/中创建规则文件，使用YAML前置元数据指定glob模式，根据文件路径有条件地应用约定
- B) Consolidate all conventions in the root CLAUDE.md file under headers for each area, relying on Claude to infer which section applies
  将所有约定整合到根CLAUDE.md文件中，按区域设置标题，依赖Claude推断哪个部分适用
- C) Create skills in .claude/skills/ for each code type that include the relevant conventions in their SKILL.md files
  在.claude/skills/中为每种代码类型创建技能，在其SKILL.md文件中包含相关约定
- D) Place a separate CLAUDE.md file in each subdirectory containing that area's specific conventions
  在每个子目录中放置单独的CLAUDE.md文件，包含该区域的特定约定

> **Correct Answer:** A

**Explanation:** Option A is correct because .claude/rules/ with glob patterns (e.g., **/*.test.tsx) allows conventions to be automatically applied based on file paths regardless of directory location—essential for test files spread throughout the codebase. Option B relies on inference rather than explicit matching, making it unreliable. Option C requires manual skill invocation or relies on Claude choosing to load them, contradicting the need for deterministic "automatic" application based on file paths. Option D can't easily handle files spread across many directories since CLAUDE.md files are directory-bound.

> 解析：选项A正确，因为带有glob模式（例如**/*.test.tsx）的.claude/rules/允许根据文件路径自动应用约定，无论目录位置如何——这对于分散在整个代码库中的测试文件至关重要。选项B依赖推断而非显式匹配，使其不可靠。选项C需要手动调用技能或依赖Claude选择加载它们，这与基于文件路径的确定性"自动"应用需求相矛盾。选项D无法轻松处理分布在许多目录中的文件，因为CLAUDE.md文件是目录绑定的。

### Scenario: Multi-Agent Research System

**Question 7: After running the system on the topic "impact of AI on creative industries," you observe that each subagent completes successfully: the web search agent finds relevant articles, the document analysis agent summarizes papers correctly, and the synthesis agent produces coherent output. However, the final reports cover only visual arts, completely missing music, writing, and film production. When you examine the coordinator's logs, you see it decomposed the topic into three subtasks: "AI in digital art creation," "AI in graphic design," and "AI in photography." What is the most likely root cause?**

> 问题7：在"AI对创意产业的影响"主题上运行系统后，你观察到每个子代理都成功完成：网络搜索代理找到相关文章，文档分析代理正确总结论文，合成代理产生连贯输出。然而，最终报告仅涵盖视觉艺术，完全遗漏音乐、写作和电影制作。当你检查协调器的日志时，你看到它将主题分解为三个子任务："数字艺术创作中的AI"、"平面设计中的AI"和"摄影中的AI"。最可能的根本原因是什么？

- A) The synthesis agent lacks instructions for identifying coverage gaps in the findings it receives from other agents.
  合成代理缺乏识别从其他代理接收的发现中覆盖缺口的指令。
- B) The coordinator agent's task decomposition is too narrow, resulting in subagent assignments that don't cover all relevant domains of the topic.
  协调器代理的任务分解过于狭窄，导致子代理分配未能覆盖主题的所有相关领域。
- C) The web search agent's queries are not comprehensive enough and need to be expanded to cover more creative industry sectors.
  网络搜索代理的查询不够全面，需要扩展以涵盖更多创意产业领域。
- D) The document analysis agent is filtering out sources related to non-visual creative industries due to overly restrictive relevance criteria.
  文档分析代理由于过于严格的相关性标准而过滤掉与非视觉创意产业相关的来源。

> **Correct Answer:** B

**Explanation:** The coordinator's logs reveal the root cause directly: it decomposed "creative industries" into only visual arts subtasks (digital art, graphic design, photography), completely omitting music, writing, and film. The subagents executed their assigned tasks correctly—the problem is what they were assigned. Options A, C, and D incorrectly blame downstream agents that are working correctly within their assigned scope.

> 解析：协调器的日志直接揭示了根本原因：它将"创意产业"分解为仅视觉艺术的子任务（数字艺术、平面设计、摄影），完全遗漏了音乐、写作和电影。子代理正确执行了分配的任务——问题在于分配的任务内容。选项A、C和D错误地指责了在其分配范围内正常工作的下游代理。

**Question 8: The web search subagent times out while researching a complex topic. You need to design how this failure information flows back to the coordinator agent. Which error propagation approach best enables intelligent recovery?**

> 问题8：网络搜索子代理在研究复杂主题时超时。你需要设计此故障信息如何流回协调器代理。哪种错误传播方法最有利于智能恢复？

- A) Return structured error context to the coordinator including the failure type, the attempted query, any partial results, and potential alternative approaches.
  向协调器返回结构化错误上下文，包括故障类型、尝试的查询、任何部分结果和潜在的替代方法。
- B) Implement automatic retry logic with exponential backoff within the subagent, returning a generic "search unavailable" status only after all retries are exhausted.
  在子代理内部实现带指数退避的自动重试逻辑，仅在所有重试用尽后返回通用的"搜索不可用"状态。
- C) Catch the timeout within the subagent and return an empty result set marked as successful.
  在子代理内部捕获超时，并返回标记为成功的空结果集。
- D) Propagate the timeout exception directly to a top-level handler that terminates the entire research workflow.
  将超时异常直接传播到终止整个研究工作流的顶层处理程序。

> **Correct Answer:** A

**Explanation:** Structured error context gives the coordinator the information it needs to make intelligent recovery decisions—whether to retry with a modified query, try an alternative approach, or proceed with partial results. Option B's generic status hides valuable context from the coordinator, preventing informed decisions. Option C suppresses the error by marking failure as success, which prevents any recovery and risks incomplete research outputs. Option D terminates the entire workflow unnecessarily when recovery strategies could succeed.

> 解析：结构化错误上下文为协调器提供做出智能恢复决策所需的信息——无论是使用修改的查询重试、尝试替代方法，还是继续使用部分结果。选项B的通用状态向协调器隐藏了有价值的上下文，阻碍了明智的决策。选项C通过将失败标记为成功来抑制错误，这阻止了任何恢复并可能导致不完整的研究输出。选项D在恢复策略可能成功时不必要地终止整个工作流。

**Question 9: During testing, you observe that the synthesis agent frequently needs to verify specific claims while combining findings. Currently, when verification is needed, the synthesis agent returns control to the coordinator, which invokes the web search agent, then re-invokes synthesis with results. This adds 2-3 round trips per task and increases latency by 40%. Your evaluation shows that 85% of these verifications are simple fact-checks (dates, names, statistics) while 15% require deeper investigation. What's the most effective approach to reduce overhead while maintaining system reliability?**

> 问题9：在测试期间，你观察到合成代理在组合发现时经常需要验证特定主张。目前，当需要验证时，合成代理将控制权返回给协调器，协调器调用网络搜索代理，然后使用结果重新调用合成代理。这为每个任务增加了2-3轮往返，并将延迟增加了40%。你的评估显示，这些验证中85%是简单的事实检查（日期、姓名、统计数据），而15%需要更深入的调查。在保持系统可靠性的同时减少开销的最有效方法是什么？

- A) Give the synthesis agent a scoped verify_fact tool for simple lookups, while complex verifications continue delegating to the web search agent through the coordinator.
  为合成代理提供一个有范围的verify_fact工具用于简单查找，而复杂验证继续通过协调器委托给网络搜索代理。
- B) Have the synthesis agent accumulate all verification needs and return them as a batch to the coordinator at the end of its pass, which then sends them all to the web search agent at once.
  让合成代理积累所有验证需求，在其处理结束时批量返回给协调器，然后协调器一次性将它们全部发送给网络搜索代理。
- C) Give the synthesis agent access to all web search tools so it can handle any verification need directly without round-trips through the coordinator.
  让合成代理访问所有网络搜索工具，以便它可以直接处理任何验证需求，无需通过协调器往返。
- D) Have the web search agent proactively cache extra context around each source during initial research, anticipating what the synthesis agent might need to verify.
  让网络搜索代理在初始研究期间主动缓存每个来源的额外上下文，预测合成代理可能需要验证的内容。

> **Correct Answer:** A

**Explanation:** Option A applies the principle of least privilege by giving the synthesis agent only what it needs for the 85% common case (simple fact verification) while preserving the existing coordination pattern for complex cases. Option B's batching approach creates blocking dependencies since synthesis steps may depend on earlier verified facts. Option C over-provisions the synthesis agent, violating separation of concerns. Option D relies on speculative caching that cannot reliably predict what the synthesis agent will need to verify.

> 解析：选项A应用最小权限原则，仅向合成代理提供85%常见情况（简单事实验证）所需的内容，同时为复杂情况保留现有的协调模式。选项B的批处理方法创建了阻塞依赖，因为合成步骤可能依赖于较早验证的事实。选项C过度配置合成代理，违反了关注点分离原则。选项D依赖于推测性缓存，无法可靠预测合成代理需要验证的内容。

### Scenario: Claude Code for Continuous Integration

**Question 10: Your pipeline script runs claude "Analyze this pull request for security issues" but the job hangs indefinitely. Logs indicate Claude Code is waiting for interactive input. What's the correct approach to run Claude Code in an automated pipeline?**

> 问题10：你的流水线脚本运行 claude "Analyze this pull request for security issues"，但作业无限期挂起。日志显示Claude Code正在等待交互式输入。在自动化流水线中运行Claude Code的正确方法是什么？

- A) Add the -p flag: claude -p "Analyze this pull request for security issues"
  添加-p标志：claude -p "Analyze this pull request for security issues"
- B) Set the environment variable CLAUDE_HEADLESS=true before running the command
  在运行命令前设置环境变量 CLAUDE_HEADLESS=true
- C) Redirect stdin from /dev/null: claude "Analyze this pull request for security issues" < /dev/null
  从/dev/null重定向stdin：claude "Analyze this pull request for security issues" < /dev/null
- D) Add the --batch flag: claude --batch "Analyze this pull request for security issues"
  添加--batch标志：claude --batch "Analyze this pull request for security issues"

> **Correct Answer:** A

**Explanation:** The -p (or --print) flag is the documented way to run Claude Code in non-interactive mode. It processes the prompt, outputs the result to stdout, and exits without waiting for user input—exactly what CI/CD pipelines require. The other options reference non-existent features (CLAUDE_HEADLESS environment variable, --batch flag) or use Unix workarounds that don't properly address Claude Code's command syntax.

> 解析：-p（或--print）标志是运行Claude Code非交互模式的文档化方式。它处理提示，将结果输出到stdout，然后退出而不等待用户输入——这正是CI/CD流水线所需的。其他选项引用了不存在的功能（CLAUDE_HEADLESS环境变量、--batch标志）或使用不能正确处理Claude Code命令语法的Unix变通方法。

**Question 11: Your team wants to reduce API costs for automated analysis. Currently, real-time Claude calls power two workflows: (1) a blocking pre-merge check that must complete before developers can merge, and (2) a technical debt report generated overnight for review the next morning. Your manager proposes switching both to the Message Batches API for its 50% cost savings. How should you evaluate this proposal?**

> 问题11：你的团队希望降低自动化分析的API成本。目前，实时Claude调用支持两个工作流：（1）必须在开发者合并前完成的阻塞性预合并检查，以及（2）夜间生成供次日早晨审查的技术债务报告。你的经理建议将两者都切换到Message Batches API以获得50%的成本节约。你应该如何评估这个提议？

- A) Use batch processing for the technical debt reports only; keep real-time calls for pre-merge checks.
  仅对技术债务报告使用批处理；预合并检查保持实时调用。
- B) Switch both workflows to batch processing with status polling to check for completion.
  将两个工作流都切换到批处理，并通过轮询状态来检查完成情况。
- C) Keep real-time calls for both workflows to avoid batch result ordering issues.
  对两个工作流都保持实时调用，以避免批处理结果排序问题。
- D) Switch both to batch processing with a timeout fallback to real-time if batches take too long.
  将两者都切换到批处理，如果批处理耗时过长则回退到实时调用。

> **Correct Answer:** A

**Explanation:** The Message Batches API offers 50% cost savings but has processing times up to 24 hours with no guaranteed latency SLA. This makes it unsuitable for blocking pre-merge checks where developers wait for results, but ideal for overnight batch jobs like technical debt reports. Option B is wrong because relying on "often faster" completion isn't acceptable for blocking workflows. Option C reflects a misconception—batch results can be correlated using custom_id fields. Option D adds unnecessary complexity when the simpler solution is matching each API to its appropriate use case.

> 解析：Message Batches API提供50%的成本节约，但处理时间长达24小时且没有保证的延迟SLA。这使得它不适合开发者等待结果的阻塞性预合并检查，但非常适合像技术债务报告这样的夜间批处理作业。选项B错误，因为依赖"通常更快"的完成时间对于阻塞性工作流来说是不可接受的。选项C反映了一种误解——批处理结果可以使用custom_id字段进行关联。选项D增加了不必要的复杂性，而更简单的解决方案是为每个API匹配其适当的用例。

**Question 12: A pull request modifies 14 files across the stock tracking module. Your single-pass review analyzing all files together produces inconsistent results: detailed feedback for some files but superficial comments for others, obvious bugs missed, and contradictory feedback—flagging a pattern as problematic in one file while approving identical code elsewhere in the same PR. How should you restructure the review?**

> 问题12：一个拉取请求修改了库存跟踪模块中的14个文件。你的一次性审查同时分析所有文件产生不一致的结果：对某些文件有详细反馈，对其他文件则有浅显评论，明显错误被遗漏，矛盾反馈——在一个文件中将某种模式标记为有问题，而在同一PR的其他地方却批准了相同的代码。你应该如何重组审查？

- A) Split into focused passes: analyze each file individually for local issues, then run a separate integration-focused pass examining cross-file data flow.
  拆分为专注的审查轮次：单独分析每个文件的本地问题，然后运行单独的专注于集成的审查轮次检查跨文件数据流。
- B) Require developers to split large PRs into smaller submissions of 3-4 files before the automated review runs.
  要求开发者在自动审查运行前将大型PR拆分为3-4个文件的小型提交。
- C) Switch to a higher-tier model with a larger context window to give all 14 files adequate attention in one pass.
  切换到具有更大上下文窗口的高层模型，以便在一次审查中给予所有14个文件足够的关注。
- D) Run three independent review passes on the full PR and only flag issues that appear in at least two of the three runs.
  对完整PR运行三个独立的审查轮次，仅标记在至少两个轮次中出现的问题。

> **Correct Answer:** A

**Explanation:** Splitting reviews into focused passes directly addresses the root cause: attention dilution when processing many files at once. File-by-file analysis ensures consistent depth, while a separate integration pass catches cross-file issues. Option B shifts burden to developers without improving the system. Option C misunderstands that larger context windows don't solve attention quality issues. Option D would actually suppress detection of real bugs by requiring consensus on issues that may only be caught intermittently.

> 解析：将审查拆分为专注的审查轮次直接解决了根本原因：同时处理多个文件时的注意力分散。逐文件分析确保一致的深度，而单独的集成审查轮次捕捉跨文件问题。选项B将负担转移给开发者而没有改进系统。选项C误解了更大的上下文窗口并不能解决注意力质量问题。选项D实际上会抑制真实错误的检测，因为它要求对可能仅被间歇性捕捉的问题达成共识。

## Preparation Exercises

Complete these hands-on exercises to build practical familiarity with the topics covered on the exam. Each exercise is designed to reinforce knowledge across one or more exam domains.

> 完成这些实践练习，以建立对考试涵盖主题的熟悉度。每个练习都旨在加强一个或多个考试领域的知识。

### Exercise 1: Build a Multi-Tool Agent with Escalation Logic

**Objective:** Practice designing an agentic loop with tool integration, structured error handling, and escalation patterns.

> **目标：** 练习设计具有工具集成、结构化错误处理和升级模式的代理循环。

**Steps:**

> **步骤：**

1. Define 3-4 MCP tools with detailed descriptions that clearly differentiate each tool's purpose, expected inputs, and boundary conditions. Include at least two tools with similar functionality that require careful description to avoid selection confusion.
   定义3-4个具有详细描述的MCP工具，清晰区分每个工具的用途、预期输入和边界条件。至少包含两个具有相似功能的工具，需要仔细描述以避免选择混淆。
2. Implement an agentic loop that checks stop_reason to determine whether to continue tool execution or present the final response. Handle both "tool_use" and "end_turn" stop reasons correctly.
   实现检查stop_reason的代理循环，以确定是继续工具执行还是呈现最终响应。正确处理"tool_use"和"end_turn"两种停止原因。
3. Add structured error responses to your tools: include errorCategory (transient/validation/permission), isRetryable boolean, and human-readable descriptions. Test that the agent handles each error type appropriately (retrying transient errors, explaining business errors to the user).
   为工具添加结构化错误响应：包含errorCategory（transient/validation/permission）、isRetryable布尔值和人类可读的描述。测试代理是否正确处理每种错误类型（重试临时错误，向用户解释业务错误）。
4. Implement a programmatic hook that intercepts tool calls to enforce a business rule (e.g., blocking operations above a threshold amount), redirecting to an escalation workflow when triggered.
   实现一个程序化钩子来拦截工具调用以强制执行业务规则（例如，阻止超过阈值的操作），在触发时重定向到升级工作流。
5. Test with multi-concern messages (e.g., requests involving multiple issues) and verify the agent decomposes the request, handles each concern, and synthesizes a unified response.
   使用多关注点消息（例如，涉及多个问题的请求）进行测试，并验证代理分解请求、处理每个关注点并综合统一响应。

**Domains reinforced:** Domain 1 (Agentic Architecture & Orchestration), Domain 2 (Tool Design & MCP Integration), Domain 5 (Context Management & Reliability)

> **强化的领域：** 领域1（代理架构与编排）、领域2（工具设计与MCP集成）、领域5（上下文管理与可靠性）

### Exercise 2: Configure Claude Code for a Team Development Workflow

**Objective:** Practice configuring CLAUDE.md hierarchies, custom slash commands, path-specific rules, and MCP server integration for a multi-developer project.

> **目标：** 练习为多开发者项目配置CLAUDE.md层次结构、自定义斜杠命令、路径特定规则和MCP服务器集成。

**Steps:**

> **步骤：**

1. Create a project-level CLAUDE.md with universal coding standards and testing conventions. Verify that instructions placed at the project level are consistently applied across all team members.
   创建具有通用编码标准和测试约定的项目级CLAUDE.md。验证放置在项目级别的指令是否一致地应用于所有团队成员。
2. Create .claude/rules/ files with YAML frontmatter glob patterns for different code areas (e.g., paths: ["src/api/**/*"] for API conventions, paths: ["**/*.test.*"] for testing conventions). Test that rules load only when editing matching files.
   创建带有YAML前置元数据glob模式的.claude/rules/文件，用于不同的代码区域（例如，paths: ["src/api/**/*"]用于API约定，paths: ["**/*.test.*"]用于测试约定）。测试规则是否仅在编辑匹配文件时加载。
3. Create a project-scoped skill in .claude/skills/ with context: fork and allowed-tools restrictions. Verify the skill runs in isolation without polluting the main conversation context.
   在.claude/skills/中创建具有context: fork和allowed-tools限制的项目作用域技能。验证技能在隔离环境中运行，不会污染主对话上下文。
4. Configure an MCP server in .mcp.json with environment variable expansion for credentials. Add a personal experimental MCP server in ~/.claude.json and verify both are available simultaneously.
   在.mcp.json中配置具有凭证环境变量扩展的MCP服务器。在~/.claude.json中添加个人实验性MCP服务器，并验证两者同时可用。
5. Test plan mode versus direct execution on tasks of varying complexity: a single-file bug fix, a multi-file library migration, and a new feature with multiple valid implementation approaches. Observe when plan mode provides value.
   测试不同复杂度任务的计划模式与直接执行：单文件bug修复、多文件库迁移以及具有多种有效实现方法的新功能。观察计划模式何时提供价值。

**Domains reinforced:** Domain 3 (Claude Code Configuration & Workflows), Domain 2 (Tool Design & MCP Integration)

> **强化的领域：** 领域3（Claude Code配置与工作流）、领域2（工具设计与MCP集成）

### Exercise 3: Build a Structured Data Extraction Pipeline

**Objective:** Practice designing JSON schemas, using tool_use for structured output, implementing validation-retry loops, and designing batch processing strategies.

> **目标：** 练习设计JSON模式、使用tool_use进行结构化输出、实施验证-重试循环以及设计批处理策略。

**Steps:**

> **步骤：**

1. Define an extraction tool with a JSON schema containing required and optional fields, an enum with an "other" + detail string pattern, and nullable fields for information that may not exist in source documents. Process documents where some fields are absent and verify the model returns null rather than fabricating values.
   定义一个具有JSON模式的提取工具，包含必需和可选字段、具有"other" +详细字符串模式的枚举，以及可能不存在于源文档中的信息的可空字段。处理某些字段缺失的文档，并验证模型返回null而不是编造值。
2. Implement a validation-retry loop: when Pydantic or JSON schema validation fails, send a follow-up request including the document, the failed extraction, and the specific validation error. Track which errors are resolvable via retry (format mismatches) versus which are not (information absent from source).
   实现验证-重试循环：当Pydantic或JSON模式验证失败时，发送后续请求，包含文档、失败的提取和特定的验证错误。跟踪哪些错误可以通过重试解决（格式不匹配），哪些不能（信息缺失于源中）。
3. Add few-shot examples demonstrating extraction from documents with varied formats (e.g., inline citations vs bibliographies, narrative descriptions vs structured tables) and verify improved handling of structural variety.
   添加少样本示例，展示从不同格式的文档中提取（例如，行内引用 vs 参考文献、叙事描述 vs 结构化表格），并验证结构多样性的改进处理。
4. Design a batch processing strategy: submit a batch of 100 documents using the Message Batches API, handle failures by custom_id, resubmit failed documents with modifications (e.g., chunking oversized documents), and calculate total processing time relative to SLA constraints.
   设计批处理策略：使用Message Batches API提交100个文档的批次，按custom_id处理失败，重新提交带有修改的失败文档（例如，分块过大的文档），并根据SLA约束计算总处理时间。
5. Implement a human review routing strategy: have the model output field-level confidence scores, route low-confidence extractions to human review, and analyze accuracy by document type and field to verify consistent performance.
   实施人工审查路由策略：让模型输出字段级置信度分数，将低置信度提取路由到人工审查，并按文档类型和字段分析准确性以验证一致的性能。

**Domains reinforced:** Domain 4 (Prompt Engineering & Structured Output), Domain 5 (Context Management & Reliability)

> **强化的领域：** 领域4（提示工程与结构化输出）、领域5（上下文管理与可靠性）

### Exercise 4: Design and Debug a Multi-Agent Research Pipeline

**Objective:** Practice orchestrating subagents, managing context passing, implementing error propagation, and handling synthesis with provenance tracking.

> **目标：** 练习编排子代理、管理上下文传递、实施错误传播以及处理带有来源跟踪的综合。

**Steps:**

> **步骤：**

1. Build a coordinator agent that delegates to at least two subagents (e.g., web search and document analysis). Ensure the coordinator's allowedTools includes "Task" and that each subagent receives its research findings directly in its prompt rather than relying on automatic context inheritance.
   构建一个委托给至少两个子代理（例如，网络搜索和文档分析）的协调器代理。确保协调器的allowedTools包含"Task"，并且每个子代理在其提示中直接接收其研究结果，而不是依赖自动上下文继承。
2. Implement parallel subagent execution by having the coordinator emit multiple Task tool calls in single response. Measure the latency improvement compared to sequential execution.
   通过让协调器在单个响应中发出多个Task工具调用来实现并行子代理执行。测量与顺序执行相比的延迟改进。
3. Design structured output for subagents that separates content from metadata: each finding should include a claim, evidence excerpt, source URL/document name, and publication date. Verify that the synthesis subagent preserves source attribution when combining findings.
   为子代理设计将内容与元数据分离的结构化输出：每个发现应包含主张、证据摘录、来源URL/文档名称和出版日期。验证合成代理在组合发现时保留来源归属。
4. Implement error propagation: simulate a subagent timeout and verify the coordinator receives structured error context (failure type, attempted query, partial results). Test that the coordinator can proceed with partial results and annotate the final output with coverage gaps.
   实施错误传播：模拟子代理超时，并验证协调器接收结构化错误上下文（故障类型、尝试的查询、部分结果）。测试协调器是否可以继续使用部分结果并在最终输出中标注覆盖缺口。
5. Test with conflicting source data (e.g., two credible sources with different statistics) and verify the synthesis output preserves both values with source attribution rather than arbitrarily selecting one, and structures the report to distinguish well-established from contested findings.
   使用冲突的源数据（例如，两个具有不同统计数据的可信来源）进行测试，并验证合成输出保留两个值并带有来源归属，而不是任意选择一个，并结构化报告以区分已确立的发现和有争议的发现。

**Domains reinforced:** Domain 1 (Agentic Architecture & Orchestration), Domain 2 (Tool Design & MCP Integration), Domain 5 (Context Management & Reliability)

> **强化的领域：** 领域1（代理架构与编排）、领域2（工具设计与MCP集成）、领域5（上下文管理与可靠性）

## Appendix

### Technologies and Concepts

The following list contains technologies and concepts that might appear on the exam:

> 以下列表包含可能出现在考试中的技术和概念：

- Claude Agent SDK — Agent definitions, agentic loops, stop_reason handling, hooks (PostToolUse, tool call interception), subagent spawning via Task tool, allowedTools configuration
- Model Context Protocol (MCP) — MCP servers, MCP tools, MCP resources, isError flag, tool descriptions, tool distribution, .mcp.json configuration, environment variable expansion
- Claude Code — CLAUDE.md configuration hierarchy (user/project/directory), .claude/rules/ with YAML frontmatter path-scoping, .claude/commands/ for slash commands, .claude/skills/ with SKILL.md frontmatter (context: fork, allowed-tools, argument-hint), plan mode, direct execution, /memory command, /compact, --resume, fork_session, Explore subagent
- Claude Code CLI — -p / --print flag for non-interactive mode, --output-format json, --json-schema for structured CI output
- Claude API — tool_use with JSON schemas, tool_choice options ("auto", "any", forced tool selection), stop_reason values ("tool_use", "end_turn"), max_tokens, system prompts
- Message Batches API — 50% cost savings, up to 24-hour processing window, custom_id for request/response correlation, polling for completion, no multi-turn tool calling support
- JSON Schema — Required vs optional fields, enum types, nullable fields, "other" + detail string patterns, strict mode for syntax error elimination
- Pydantic — Schema validation, semantic validation errors, validation-retry loops
- Built-in tools — Read, Write, Edit, Bash, Grep, Glob — their purposes and selection criteria
- Few-shot prompting — Targeted examples for ambiguous scenarios, format demonstration, generalization to novel patterns
- Prompt chaining — Sequential task decomposition into focused passes
- Context window management — Token budgets, progressive summarization, lost-in-the-middle effects, context extraction, scratchpad files
- Session management — Session resumption, fork_session, named sessions, session context isolation
- Confidence scoring — Field-level confidence, calibration with labeled validation sets, stratified sampling for error rate measurement

### In-Scope Topics

The following topics are explicitly tested on the exam:

> 以下主题明确在考试中测试：

- Agentic loop implementation: Control flow based on stop_reason, tool result handling, loop termination conditions
- Multi-agent orchestration: Coordinator-subagent patterns, task decomposition, parallel subagent execution, iterative refinement loops
- Subagent context management: Explicit context passing, structured state persistence, crash recovery using manifests
- Tool interface design: Writing effective tool descriptions, splitting vs consolidating tools, tool naming to reduce ambiguity
- MCP tool and resource design: Resources for content catalogs, tools for actions, description quality for adoption
- MCP server configuration: Project vs user scope, environment variable expansion, multi-server simultaneous access
- Error handling and propagation: Structured error responses, transient vs business vs permission errors, local recovery before escalation
- Escalation decision-making: Explicit criteria, honoring customer preferences, policy gap identification
- CLAUDE.md configuration: Hierarchy (user/project/directory), @import patterns, .claude/rules/ with glob patterns
- Custom commands and skills: Project vs user scope, context: fork, allowed-tools, argument-hint frontmatter
- Plan mode vs direct execution: Complexity assessment, architectural decisions, single-file changes
- Iterative refinement: Input/output examples, test-driven iteration, interview pattern, sequential vs parallel issue resolution
- Structured output via tool_use: Schema design, tool_choice configuration, nullable fields to prevent hallucination
- Few-shot prompting: Ambiguous scenario targeting, format consistency, false positive reduction
- Batch processing: Message Batches API appropriateness, latency tolerance assessment, failure handling by custom_id
- Context window optimization: Trimming verbose tool outputs, structured fact extraction, position-aware input ordering
- Human review workflows: Confidence calibration, stratified sampling, accuracy segmentation by document type and field
- Information provenance: Claim-source mappings, temporal data handling, conflict annotation, coverage gap reporting

## 6. Out-of-Scope Topics

The following related topics will NOT appear on the exam:

> 以下相关主题**不会**出现在考试中：

- Fine-tuning Claude models or training custom models
- Claude API authentication, billing, or account management
- Detailed implementation of specific programming languages or frameworks (beyond what's needed for tool and schema configuration)
- Deploying or hosting MCP servers (infrastructure, networking, container orchestration)
- Claude's internal architecture, training process, or model weights
- Constitutional AI, RLHF, or safety training methodologies
- Embedding models or vector database implementation details
- Computer use (browser automation, desktop interaction)
- Vision/image analysis capabilities
- Streaming API implementation or server-sent events
- Rate limiting, quotas, or API pricing calculations
- OAuth, API key rotation, or authentication protocol details
- Specific cloud provider configurations (AWS, GCP, Azure)
- Performance benchmarking or model comparison metrics
- Prompt caching implementation details (beyond knowing it exists)
- Token counting algorithms or tokenization specifics

## 7. Exam Preparation Recommendations

To prepare for this certification exam:

> 要为这个认证考试做准备：

1. Build an agent with the Claude Agent SDK: Implement a complete agentic loop with tool calling, error handling, and session management. Practice spawning subagents and passing context between them.
   使用Claude Agent SDK构建代理：实现完整的代理循环，包括工具调用、错误处理和会话管理。练习生成子代理并在它们之间传递上下文。
2. Configure Claude Code for a real project: Set up CLAUDE.md with a configuration hierarchy, create path-specific rules in .claude/rules/, build custom skills with frontmatter options (context: fork, allowed-tools), and integrate at least one MCP server.
   为真实项目配置Claude Code：使用配置层次结构设置CLAUDE.md，在.claude/rules/中创建路径特定规则，使用前置元数据选项构建自定义技能（context: fork, allowed-tools），并集成至少一个MCP服务器。
3. Design and test MCP tools: Write tool descriptions that clearly differentiate similar tools. Implement structured error responses with error categories and retryable flags. Test tool selection reliability with ambiguous requests.
   设计和测试MCP工具：编写能够清楚区分相似工具的工具描述。实施具有错误类别和可重试标志的结构化错误响应。使用模糊请求测试工具选择可靠性。
4. Build a structured data extraction pipeline: Use tool_use with JSON schemas, implement validation-retry loops, design schemas with optional/nullable fields, and practice batch processing with the Message Batches API.
   构建结构化数据提取管道：使用tool_use和JSON模式，实施验证-重试循环，设计具有可选/可空字段的模式，并使用Message Batches API练习批处理。
5. Practice prompt engineering techniques: Write few-shot examples for ambiguous scenarios. Define explicit review criteria to reduce false positives. Design multi-pass review architectures for large code reviews.
   练习提示工程技术：为模糊场景编写少样本示例。定义明确的审查标准以减少误报。为大型代码审查设计多轮审查架构。
6. Study context management patterns: Practice extracting structured facts from verbose tool outputs, implementing scratchpad files for long sessions, and designing subagent delegation to manage context limits.
   学习上下文管理模式：从冗长的工具输出中提取结构化事实，为长会话实施草稿板文件，并设计子代理委托以管理上下文限制。
7. Review escalation and human-in-the-loop patterns: Understand when to escalate (policy gaps, customer requests, inability to progress) versus resolve autonomously. Practice designing human review workflows with confidence-based routing.
   审查升级和人机协同模式：了解何时升级（政策缺口、客户请求、无法进展）与自主解决。练习设计具有基于置信度路由的人工审查工作流。
8. Complete the Practice Exam: Before sitting for the real exam, complete the practice exam (the link will be provided separately). The practice exam covers the same scenarios and question format as the real exam and shows explanations after each answer to help reinforce your understanding.
   完成练习考试：在参加考试之前，完成练习考试（链接将单独提供）。练习考试涵盖与真实考试相同的场景和问题格式，并在每个答案后显示解释，以帮助加强你的理解。

Version 0.1 Last Updated: Feb 10 2025

> 版本0.1 最后更新：2025年2月10日
