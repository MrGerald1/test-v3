# Claude Code Configuration for coolbeginner

## gstack

This project uses **gstack** — Garry Tan's open-source software factory for AI-driven development. gstack provides structured roles and workflows that augment Claude Code with specialized skills.

### Available Skills

For all web browsing tasks, use the `/browse` skill from gstack (never use mcp__claude-in-chrome-* tools).

**Development & Planning:**
- `/office-hours` — Brainstorm and reframe feature ideas
- `/plan-ceo-review` — Validate strategy and product scope
- `/plan-eng-review` — Design architecture and system diagrams
- `/plan-design-review` — Review design and visual specs
- `/design-consultation` — Build or review design systems

**Code & Quality:**
- `/review` — Code review before merge (auto-fix + ask for decisions)
- `/ship` — Create PR with tests and release checklist
- `/qa` — QA testing on staging URLs (real browser)
- `/qa-only` — Quick QA spot checks
- `/investigate` — Debug errors and diagnose issues
- `/design-review` — Visual design audit and checks

**Operations & Releases:**
- `/retro` — Weekly retrospective and stats
- `/document-release` — Post-ship documentation updates

**Expert Review:**
- `/codex` — Adversarial code review and second opinions
- `/careful` — Maximum safety mode for production systems

**Safety & Control:**
- `/freeze` — Scope edits to one module/directory
- `/guard` — Maximum safety mode with destructive warnings
- `/unfreeze` — Remove edit restrictions

**Maintenance:**
- `/gstack-upgrade` — Upgrade gstack to latest version
- `/setup-browser-cookies` — Configure browser authentication

### Setup

If gstack skills aren't working, run:

```bash
cd .claude/skills/gstack && ./setup
```

This will rebuild binaries and register skills.

### Documentation

Read more about gstack: https://github.com/garrytan/gstack

---

## General Guidelines

- Use gstack skills proactively when appropriate
- Always run `/review` before creating PRs
- Use `/qa` to verify deployments on staging
- Follow the "Boil the Lake" principle — complete the whole thing when the marginal cost is near-zero
