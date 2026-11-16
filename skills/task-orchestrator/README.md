# Task Orchestrator

让 AI 根据目标选择已有技能、按需寻找外部技能，并完成交付与检查。

An agent skill that selects existing skills, discovers missing capabilities, and coordinates a workflow through a checked deliverable.

## 工作方式 / Workflow

1. 明确目标、受众与交付格式。
2. 动态读取当前技能库，选择最少且适用的技能组合。
3. 按依赖顺序完成研究、分析、写作与文件制作。
4. 能力不足时搜索外部技能，检查实际说明、源码与依赖。
5. 检查结果，交付文件或链接，并说明尚未解决的限制。

It uses the current skill catalog rather than a fixed inventory. It respects available tools, permissions, explicit-only skills, and authorization for installation or publishing. It does not include or redistribute the skills it may select.

## 安装 / Installation

Download this repository and copy the complete `skills/task-orchestrator` folder, including `references`, into your Codex skills directory:

```text
~/.codex/skills/task-orchestrator/SKILL.md
```

On Windows, the default location is `%USERPROFILE%\.codex\skills\task-orchestrator\SKILL.md`. If your setup uses a custom skills directory, use that location instead.

## 使用示例 / Usage

```text
用 $task-orchestrator 调研一家目标公司，分析合作机会，
并制作一份中文客户提案 PPT，附上关键事实的来源。
```

```text
Use $task-orchestrator to research a topic, draft a cited brief,
and produce a presentation using suitable available skills.
```

## Requirements and limitations

- Requires an agent host capable of reading skill instructions and executing relevant tools.
- Research, image generation, document creation, and connected apps depend on the host's available capabilities and accounts.
- External skill installation is subject to the user's authorization and environment permissions.
- This is an instruction-based workflow, not a standalone application or background scheduler.
- Initial validation covered file structure and installation consistency. End-to-end business workflows have not yet been tested.

## ODM/CDMO workflows

The optional [ODM workflow reference](references/odm-workflows.md) covers company background checks, competitor companies, market trends, competing products, lead qualification, decision-maker mapping, nutrition-brand customer pools, and outreach preparation. It also flags regulatory/claim and manufacturing feasibility checks before proposals. External skills listed there are candidates, not bundled dependencies.

## Skill instructions

See [SKILL.md](SKILL.md) for the complete workflow.

Each change to this skill is also recorded in a separate dated document under [`updates/`](updates/).
