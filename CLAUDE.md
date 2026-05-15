# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this project is

Single-file SPA (`index.html`) — an interactive full-stack learning hub with 21 projects, 107 guided tasks, and verification commands. No build system, no dependencies, no server required.

## Running locally

```bash
open index.html          # macOS
xdg-open index.html      # Linux
```

## Validating JS syntax

The HTML file embeds all JS inline. After editing, validate with:

```bash
node --check index.html
```

No output = valid. Any output = syntax error location.

## Deploying

GitHub Pages — push to `main`, branch root. Live at:
`https://jorgearguellles.github.io/fullStackEngineer_Path/`

## Architecture

Everything lives in `index.html` in this order:
1. **CSS** — CSS variables in `:root`, dark theme, responsive grid/flexbox, no external frameworks
2. **Data constants** (large JS block mid-file):
   - `PROJECTS` — 21 project objects (`id`, `title`, `domain`, `rank`, `tags`, `stack`, `challenges`, `expandPath`)
   - `STACKS` — tech stack cards per domain
   - `TASK_GUIDE` — keyed by project `pid`, each value is an array of task objects: `{title, why, how[], cmd, tip, links[]}`
   - `VERIFY_DATA` — JSON object keyed by `[pid][taskIndex]`, each entry is `[shellCommand, expectedOutput]`. Stored as plain JSON (not template literals) to avoid shell-string escape bugs.
   - `ROADMAP`, `SKILLS`, `RESOURCES`, `TECH_RESOURCES`, `PATTERNS`
3. **Renderer functions** — `buildStacks()`, `buildProjects()`, `buildMalla()`, `buildRoadmap()`, `buildPatterns()`, `buildSkills()`, `buildResources()`, `buildVerifyHTML(pid, i)`
4. **State** — progress stored in `localStorage` keyed by project `pid` as a JSON array of checked task indices
5. **Modal system** — `openProject(p)`, `openStack(s)`, `renderChecklistInModal(pid)` for task-level detail

## Critical constraint — template literal escaping

Shell commands in `VERIFY_DATA` often contain single quotes (`'`). **Never use template literals** to build HTML that injects these strings — nested template literals with shell strings silently break the entire script. The `buildVerifyHTML` function uses string concatenation for this reason. `VERIFY_DATA` is a plain JSON object (not JS template literals) for the same reason.

## Domain color system

| Domain | CSS var | Class suffix |
|--------|---------|--------------|
| Frontend | `--fe` `#00d4ff` | `fe` |
| Backend | `--be` `#00ff9d` | `be` |
| Cloud | `--cl` `#bf7aff` | `cl` |
| AI/ML | `--ai` `#ff6b35` | `ai` |

## Adding content

To add a new project task guide: add an entry to `TASK_GUIDE[pid]` (array of task objects) and a parallel entry to `VERIFY_DATA[pid]` (array of `[command, expectedOutput]`). Projects without guide entries show an empty checklist — no crash.

Gaps to fill: `cl2`–`cl5`, `ai2`, `ai3`, `ai5` have no task guides yet.
