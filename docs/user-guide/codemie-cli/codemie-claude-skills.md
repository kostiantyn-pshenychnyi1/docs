---
id: codemie-claude-skills
title: Claude Code Skills for CodeMie
sidebar_label: Claude Code Skills
sidebar_position: 4
pagination_prev: user-guide/codemie-cli/skills-integration
pagination_next: user-guide/codemie-cli/sdk-asset-management
---

import EnterpriseFeature from '@site/src/components/EnterpriseFeature';

# Claude Code Skills for CodeMie

<EnterpriseFeature />

When you launch Claude Code with `codemie-claude`, two built-in skills are available
automatically — no additional setup required:

| Skill               | Purpose                                                                          |
| ------------------- | -------------------------------------------------------------------------------- |
| `codemie-sdk`       | Manage platform assets: assistants, workflows, datasources, integrations, skills |
| `codemie-analytics` | Access usage data, spending reports, and AI adoption leaderboards                |

Just describe what you need in natural language. Claude runs the appropriate commands for
you and handles the results.

## Prerequisites

- CodeMie CLI installed and configured (`codemie setup` completed)

## Project Selection

Before running any operation, Claude asks which project to use. It proposes your default
project (based on your account) and lets you confirm or pick a different one.

## codemie-sdk

The `codemie-sdk` skill manages all CodeMie platform assets via the `codemie sdk` CLI.

**What you can manage:** assistants, workflows, datasources, integrations, skills, users,
assistant categories, LLM models

**Example requests:**

```
Create an assistant called "Code Reviewer" in Engineering
List my datasources in the Support project
Add a Confluence datasource for space=ENG
Delete workflow <id>
Update the sql-helper skill description
List all project integrations
```

For the full list of available commands and fields, see the
[SDK CLI Reference](./sdk-asset-management).

## codemie-analytics

The `codemie-analytics` skill retrieves platform usage data and can generate self-contained
HTML reports saved to `reports/` in your working directory.

### Leaderboard and AI Champions

Track AI adoption through a scoring framework with six dimensions: platform usage, asset
creation, workflow usage, workflow authoring, CLI and agentic engineering, and knowledge
sharing. Users are ranked into tiers (pioneer, expert, advanced, practitioner, newcomer).

```
Show me the AI adoption leaderboard for Q1 2026
Who are the top 10 performers this month?
What's the tier distribution across the organization?
Give me the full champion profile for alice@company.com
```

### CLI Insights

Analyze how teams use Claude Code — session depth, tool usage, model preferences, top
repositories, and user classification by behavior type.

```
Show CLI insights for the last 30 days
Who are the top CLI users by cost?
Give me a detailed CLI profile for John_Doe
What are the usage patterns by hour and weekday?
```

### Spending and Budget

Monitor platform costs and budget utilization at the user, project, and organization level.

```
How much has Engineering spent this month?
Show me per-user spending for the last 30 days
Are any users close to their budget limits?
What's my current spend and remaining budget?
```

### General Usage Analytics

Get summaries of platform activity: conversations, assistant usage, workflow executions,
tool usage, model breakdown, and engagement patterns.

```
Give me a platform usage summary for last week
Which LLM models are used most?
Show workflow execution analytics
What tools are used most across the platform?
```

### HTML Reports

Claude can compile analytics data into a self-contained HTML report saved locally:

```
Build a leaderboard dashboard for Q1 2026
Generate a spending report for the last 30 days and save it
Create an HTML report showing CLI adoption trends
```

Reports are saved to `reports/<descriptive-name>.html` in your current working directory.
