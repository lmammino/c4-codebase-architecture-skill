# c4-codebase-architecture-skill

An agent skill for turning codebases into clear, evidence-based C4 architecture documentation.

## What it does

This skill helps an AI coding agent inspect a repository and produce [C4 model](https://c4model.com/) architecture documentation. It:

- inspects codebase evidence (entrypoints, manifests, infrastructure code, deployment descriptors, etc.)
- produces System Context, Container, and Component views
- separates observed facts from inferences
- asks targeted follow-up questions when the code alone is insufficient
- supports output as Markdown narrative with Mermaid diagrams, PlantUML, or Structurizr DSL

## Installation

### Install from npm

```bash
# npm
npx skills install npm:@lmammino/c4-codebase-architecture-skill --skill c4-codebase-architecture

# pnpm
pnpm dlx skills install npm:@lmammino/c4-codebase-architecture-skill --skill c4-codebase-architecture

# yarn (Berry / modern Yarn)
yarn dlx skills install npm:@lmammino/c4-codebase-architecture-skill --skill c4-codebase-architecture

# bun
bunx skills install npm:@lmammino/c4-codebase-architecture-skill --skill c4-codebase-architecture
```

Add `-a <agent>` if you want to target a specific agent explicitly. Otherwise, `skills` will prompt you to choose one.

### Install from GitHub

```bash
# npm
npx skills add lmammino/c4-codebase-architecture-skill --skill c4-codebase-architecture

# pnpm
pnpm dlx skills add lmammino/c4-codebase-architecture-skill --skill c4-codebase-architecture

# yarn (Berry / modern Yarn)
yarn dlx skills add lmammino/c4-codebase-architecture-skill --skill c4-codebase-architecture

# bun
bunx skills add lmammino/c4-codebase-architecture-skill --skill c4-codebase-architecture
```

### Install from a local checkout

If you already cloned this repository:

```bash
# npm
npx skills add . --skill c4-codebase-architecture

# pnpm
pnpm dlx skills add . --skill c4-codebase-architecture

# yarn (Berry / modern Yarn)
yarn dlx skills add . --skill c4-codebase-architecture

# bun
bunx skills add . --skill c4-codebase-architecture
```

Add `-g` to install globally instead of into the current project, or `-y` for a non-interactive install.

### Install the `skills` CLI globally

If you want a persistent `skills` command instead of `npx`/`dlx`/`bunx`:

```bash
# npm
npm install -g skills

# pnpm
pnpm add -g skills

# yarn (classic)
yarn global add skills

# bun
bun add -g skills
```

Then install the skill with:

```bash
skills install npm:@lmammino/c4-codebase-architecture-skill --skill c4-codebase-architecture
```

## Manual installation

You can also copy the skill directory directly into your project without using the CLI:

```bash
# Agents that use .agents/skills
cp -r skills/c4-codebase-architecture .agents/skills/

# Claude Code
cp -r skills/c4-codebase-architecture .claude/skills/

# GitHub Copilot
cp -r skills/c4-codebase-architecture .github/skills/
```

## Usage

Once installed, ask your agent to document the architecture of your codebase. Example prompts:

- *"Use the c4-codebase-architecture skill to document this repository."*
- *"Produce a C4 architecture diagram for this codebase."*
- *"Reverse engineer the system architecture from the code and give me a Container view."*

## Repository layout

```text
c4-codebase-architecture-skill/
├─ skills/
│  └─ c4-codebase-architecture/
│     └─ SKILL.md
├─ package.json
├─ README.md
└─ LICENSE
```

## License

MIT
