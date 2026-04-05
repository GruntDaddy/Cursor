# AGENTS.md

## Cursor Cloud specific instructions

### Project overview

- Project name: `[project-name]`
- Problem statement: `[what this product solves in 1-2 lines]`
- Primary users: `[who uses this]`
- Current phase: `[idea | prototype | MVP | production]`
- Explicitly out of scope: `[list non-goals to prevent incorrect assumptions]`

### Current stack

- Language/runtime: `[e.g. Node 20, Python 3.11, Go 1.22]`
- Package manager: `[npm | pnpm | yarn | pip | poetry | cargo | etc.]`
- Main framework(s): `[e.g. Next.js, FastAPI, Rails]`
- Data stores/services: `[e.g. Postgres, Redis, S3, none]`
- Deployment target: `[e.g. Vercel, AWS ECS, local only]`

### Quick start (Cursor Cloud)

Run these from repository root:

1. Install deps: `[command]`
2. Start app/service(s): `[command]`
3. Run targeted tests: `[command]`
4. Run lint/format checks: `[command]`

Required env vars (names only, never values):

- `[ENV_VAR_1]`
- `[ENV_VAR_2]`

If multiple services are required, startup order:

1. `[service A]`
2. `[service B]`
3. `[service C]`

### Testing matrix

Use the smallest high-signal test set for changed areas:

- API/backend changes: `[command]`
- UI/frontend changes: `[command]`
- Data/migrations changes: `[command]`
- Shared library changes: `[command]`

Rules:

- Do not run the entire test suite unless requested or necessary.
- Prefer targeted tests near changed files.
- For bug fixes, reproduce before fix when feasible, then verify after fix.

### Manual testing requirements

For non-trivial UI changes:

- Perform manual browser validation of the changed flow.
- Record one short demo video showing the working path end-to-end.
- Capture at least one screenshot of final expected UI state.

Suggested checklist:

- Happy path
- 1-2 key edge cases
- Error state handling
- Empty/loading states (if applicable)

### Code map

Keep this section updated as the repo grows:

- App source: `[path]`
- Tests: `[path]`
- Config: `[path]`
- Scripts/tooling: `[path]`
- Migrations/schema: `[path]`
- Static assets: `[path]`

Primary entrypoints:

- `[entrypoint 1]`
- `[entrypoint 2]`

### Conventions and guardrails

- Keep changes scoped to the request; avoid unrelated refactors.
- Do not commit temporary debug instrumentation.
- Prefer package-manager installs over manual dependency edits.
- Add/adjust tests when behavior changes.
- Preserve backward compatibility unless task explicitly allows breaking changes.

### PR and commit expectations

- One logical change per commit when practical.
- Commit message format: `[type(scope): summary]` (or project convention).
- PR description should include:
  - What changed
  - Why it changed
  - How it was tested (commands + outcomes)
  - Walkthrough artifacts for UI-impacting changes

### Troubleshooting

Document common issues and reliable fixes:

- Install failure: `[symptom]` -> `[fix]`
- Test failure: `[symptom]` -> `[fix]`
- Dev server boot issue: `[symptom]` -> `[fix]`
- Env var/setup issue: `[symptom]` -> `[fix]`

### When to update this file

Update `AGENTS.md` whenever any of these change:

- Tech stack or dependency manager
- Build/test commands
- Directory structure or entrypoints
- Required environment variables
- Team conventions for testing, commits, or PRs

### Historical note

- Refer to `git show a19c972:.cursorrules` for previously considered GDScript/Godot coding conventions.
