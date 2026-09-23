<img width="2400" height="600" alt="hero-b" src="https://github.com/user-attachments/assets/c177a82d-334b-495c-81cb-9df69c521123" />

# EvalFlow Skills

[Agent Skills](https://github.com/anthropics/skills) that teach AI coding assistants (Claude Code, Cursor, etc.) how to work with [EvalFlow](https://github.com/avijitnpm/evalflow) — the open-source LLM observability and evaluation platform for tracing, prompt management, and evaluation.

These skills interoperate with the Langfuse API, SDKs, and documentation. Originally derived from the [Langfuse skills repository](https://github.com/langfuse/skills).

## Skills

| Skill                                                           | Description                                                                                        |
| --------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| [langfuse](./skills/langfuse)                                   | Main skill to work with EvalFlow. Query and manage traces, prompts, datasets, and scores via the Langfuse API; look up documentation; do things with best practices in mind. |

## Installation

### Cursor Plugin

Install as a [Cursor plugin](https://cursor.com/docs/plugins):

```
/add-plugin langfuse
```

### skills CLI

Install via the [skills CLI](https://github.com/vercel-labs/skills):

```bash
npx skills add avijitnpm/evalflow --skill "langfuse"
```

### Manual symlink

Clone this repo and symlink the skill into your agent's skills directory:

```bash
git clone https://github.com/avijitnpm/evalflow.git /path/to/evalflow-skills
ln -s /path/to/evalflow-skills/skills/langfuse /path/to/skills-directory/langfuse
```

## Prerequisites

You need a Langfuse account ([cloud](https://cloud.langfuse.com) or [self-hosted](https://langfuse.com/docs/deployment/self-host)) and API keys:

```bash
export LANGFUSE_PUBLIC_KEY=pk-lf-...
export LANGFUSE_SECRET_KEY=sk-lf-...
export LANGFUSE_BASE_URL=https://cloud.langfuse.com  # or https://us.cloud.langfuse.com, or self-hosted URL
```

API keys are found in your Langfuse project under **Settings > API Keys**.

## Usage

Once installed, the agent will automatically use these skills when relevant — for example:

- Setting up Langfuse tracing in a project
- Setting up CI/CD experiment gates with `langfuse/experiment-action`
- Auditing existing instrumentation
- Preparing an application and Langfuse project for the v4 platform migration
- Migrating prompts to Langfuse prompt management
- Querying traces, prompts, or datasets via the API
- Looking up Langfuse docs, SDK usage, or integration guides

## Contributing

Want to improve a skill or add a new one? See [CONTRIBUTING.md](./CONTRIBUTING.md).

## Feedback & Requests

Something not working as expected, or want a new skill? [Start a discussion](https://github.com/avijitnpm/evalflow/discussions/new?category=ideas-improvements).
