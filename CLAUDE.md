# Agent Brain - Knowledge Base for AI Assistants

## Purpose
This repository is an **AI-optimized derivative** of a personal Obsidian vault. It's structured specifically for machine reading and agent context injection.

## How Agents Should Use This

1. **Start here**: Read this file first for orientation
2. **Context needed?**: Check `context/` for domain summaries
3. **Specific topic?**: Check `entities/` for structured data
4. **Recent state?**: Check `state/current.md` for latest sync
5. **Patterns?**: Check `patterns/` for recurring themes

## Directory Structure

```
/
├── CLAUDE.md           # You are here - agent orientation
├── context/            # High-level summaries by domain
│   ├── research.md     # PhD research context
│   ├── projects.md     # Active projects summary
│   └── personal.md     # Relevant personal context
├── entities/           # Structured data (people, papers, concepts)
│   ├── papers/         # Literature with frontmatter
│   ├── people/         # Key contacts/collaborators
│   └── concepts/       # Domain concepts
├── patterns/           # Recurring themes extracted from daily notes
│   ├── productivity.md # Work patterns
│   ├── blockers.md     # Common friction points
│   └── interests.md    # Topics of ongoing interest
├── state/              # Current state snapshots
│   ├── current.md      # Latest sync summary
│   └── history/        # Previous states
└── schema/             # Frontmatter schemas
    └── templates.md    # YAML templates for each entity type
```

## Frontmatter Schema

All files use standardized YAML frontmatter for machine parsing:

```yaml
---
type: [context|entity|pattern|state]
domain: [research|personal|projects]
last_updated: YYYY-MM-DD
confidence: [high|medium|low]
source: [vault_extraction|agent_inference|user_confirmed]
related: [list of related file paths]
tags: [semantic tags]
---
```

## Sync Protocol

This knowledge base is populated by automated extraction from the source vault:
- Daily notes → patterns/
- Projects → context/projects.md + entities/
- Literature notes → entities/papers/
- Zotero library → entities/papers/ (enriched)

## Source
- **Vault**: OneDrive-synced Obsidian vault
- **Sync method**: Claude Code overnight runs
- **Do not edit directly**: Changes overwritten on next sync
