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

Install the package as a development dependency:

```bash
npm install -D @lmammino/c4-codebase-architecture-skill
```

Then export the skill for your agent of choice:

```bash
# List available skills
npx agents list

# Export for GitHub Copilot
npx agents export --target copilot

# Export for Claude
npx agents export --target claude
```

The skill will be installed into the appropriate location for your agent (e.g. `.github/skills/`, `.claude/skills/`).

## Manual installation

You can also copy the skill directly into your project without npm:

```bash
# For GitHub Copilot
cp -r skills/c4-codebase-architecture .github/skills/

# For Claude
cp -r skills/c4-codebase-architecture .claude/skills/

# For any agent
cp -r skills/c4-codebase-architecture .agents/skills/
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
