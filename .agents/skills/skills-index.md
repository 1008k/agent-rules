<!-- managed-by: shared-reference -->
<!-- source-repo: https://github.com/1008k/shared-reference -->
<!-- source-path: .agents/skills/skills-index.md -->
# Shared Skills Index

Use this file as the entry point when deciding whether to use shared skills or optional supporting tools from `shared-reference`.

## How To Read

1. Start from the project `docs/policy-index.yaml`.
2. Check `.shared/shared-index.yaml` to confirm the shared reference location and lock file.
3. Read this index only when the task involves shared skills, optional tooling, context tools, MCP, memory, accessibility review, or migration cleanup.
4. Read only the relevant skill or section below.

## Shared Skills

- `docs-sync/`: Check and reconcile drift across project docs such as `docs/project-spec.md`, `README.md`, and architecture notes.
- `project-bootstrap/`: Turn an initial brief into a concrete project spec for docs-first projects.
- `web-a11y-review/`: Review and improve web accessibility for HTML, CSS, JavaScript, React, Astro, WordPress themes, landing pages, and Markdown content.

## Optional Tooling Notes

- MCP baseline: Consider MCP only when it reduces repeated lookup, external documentation drift, repository inspection cost, or operational friction. Record purpose, permissions, external communication, and failure handling in project docs when adopted.
- Context tools: Serena, Context7, Headroom, and Context Mode are useful when codebase size, documentation drift, or repeated context loading becomes costly. Prefer the narrowest tool that solves the current problem.
- GitHub/reference helpers: Use GitHub or documentation helpers when a task depends on external repositories, live issues, pull requests, or current upstream docs.
- Modern web guidance: For browser UI work, use current platform guidance and browser verification when project compatibility allows it. Keep project-specific browser support and product constraints above generic modern defaults.
- Local memory: Use lightweight memory only when repeated project context would otherwise be lost or duplicated. Do not treat memory as a substitute for current repo evidence.
- Knowledge formats: Optional formats such as Markdown plus YAML frontmatter can help when a project accumulates many reusable notes, but avoid adding a catalog before retrieval pain is real.

## Local Overrides

- Project-specific rules stay in `docs/rules-*.md`.
- Project-specific skill shims or local-only skills may use `.agents/skills/`.
- Shared skill changes should be proposed through `scripts/propose-shared-reference-change.ps1`, not edited in the vendor copy.
