# AWE Skills

> Agent Skills for [AWE Framework](https://aweframework.com) — Java/Spring Boot web application framework

[![skills.sh](https://img.shields.io/badge/skills.sh-awe--framework-blue?style=flat-square)](https://skills.sh/aweframework/awe-skills/awe-framework)
[![GitHub Repo stars](https://img.shields.io/github/stars/aweframework/awe-skills?style=flat-square)](https://github.com/aweframework/awe-skills)
[![License](https://img.shields.io/badge/License-Apache--2.0?style=flat-square)](LICENSE)

## What is this?

This repository contains **Agent Skills** for the [AWE Framework](https://aweframework.com) — a Java/Spring Boot web application framework where UI, data access, and business logic are defined through XML descriptors.

Agent Skills teach AI coding assistants (Claude Code, Cursor, OpenCode, etc.) how to work with AWE projects correctly — following the framework's conventions, patterns, and workflows.

## Available Skills

### [awe-framework](./awe-framework/SKILL.md)

Guides AI agents through AWE development:
- **XML Descriptor System** — Screens, queries, maintain, services, actions
- **Java Service Patterns** — AWE services, beans, maintain patterns
- **Project Structure** — Maven multi-module layout, conventions
- **Build & Development** — Maven commands, profiles, hot reload
- **Gitflow Workflow** — Branching, MR conventions
- **Testing** — Unit tests, integration tests

**Trigger:** When working with AWE, XML descriptors, screen XML, query XML, maintain XML, or AWE services.

## Installation

### Using the skills CLI (recommended)

```bash
# Install all skills from this repo
npx skills add aweframework/awe-skills

# Install a specific skill
npx skills add aweframework/awe-skills --skill awe-framework
```

### Manual installation

Copy `awe-framework/SKILL.md` to your agent's skills directory:

| Agent | Path |
|-------|------|
| OpenCode | `~/.config/opencode/skills/awe-framework/SKILL.md` |
| Claude Code | `~/.claude/skills/awe-framework/SKILL.md` |
| Cursor | `~/.cursor/skills/awe-framework/SKILL.md` |
| Windsurf | `~/.codeium/windsurf/skills/awe-framework/SKILL.md` |

## Quick Example

Once installed, an AI agent can understand AWE XML descriptors:

```xml
<!-- Screen XML in AWE -->
<screen id="MyScreen" template="main">
  <grid id="MyGrid" query="MyQuery" lazy="false" pagesize="20">
    <column id="id" name="lblId" />
    <column id="name" name="lblName" />
  </grid>
</screen>
```

The agent will understand the framework's conventions without you having to explain them.

## About AWE Framework

[AWE Framework](https://aweframework.com) (Almis Web Engine) is an open-source Java/Spring Boot framework that uses XML descriptors to define:

- **Screens** — UI layout and components
- **Queries** — Database access layer
- **Maintains** — CRUD operations with business logic
- **Services** — Custom Java business logic
- **Actions** — Button behaviors and server interactions

## Contributing

Contributions welcome! To add a new skill or improve existing ones:

1. Fork this repo
2. Add your skill under `skills/<your-skill>/SKILL.md`
3. Follow the [Agent Skills specification](https://agentskills.io)
4. Submit a PR

## License

Apache 2.0 — see [LICENSE](LICENSE)