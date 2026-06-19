# Eigi Skills Agent Guide

This repo stores reusable Codex skills for Eigi workflows. Keep repo-level guidance short and put detailed repeatable workflows inside skills.

## Backend Skill

Use `.codex/skills/eigi-backend-standards` when working on backend code in any Eigi repo, especially Python/FastAPI APIs, controllers, CRUD classes, services, schemas, models, logging, docstrings, or tests.

Read the skill in this order:

1. `.codex/skills/eigi-backend-standards/SKILL.md` for required backend standards.
2. `.codex/skills/eigi-backend-standards/references/folder-structure.md` before adding files or deciding layer placement.
3. `.codex/skills/eigi-backend-standards/references/examples.md` before creating or changing a router, controller, CRUD class, or service.

## Usage Rules

- Inspect nearby repo code before applying the skill.
- Follow the closest local convention first.
- Use Vaani Core as the fallback reference when the target repo has no stronger backend pattern.
- Keep every new or modified function and method documented with a docstring.
- Keep routes thin, controllers business-focused, CRUD persistence-focused, and services integration/workflow-focused.
- Add or update focused tests when backend behavior changes.

## Validation

After editing a skill, run:

```bash
python3 /Users/mrunmaychichkhede/.codex/skills/.system/skill-creator/scripts/quick_validate.py .codex/skills/eigi-backend-standards
```

Do not add per-skill `agent.md` files unless there is a specific runtime that requires them. Keep durable repo guidance here and detailed workflow instructions in `SKILL.md` plus references.
