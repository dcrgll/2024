# AGENTS.md

Defaults for AI-assisted work on this site.

Explicit user instructions and existing codebase conventions take precedence over this file.

## What this repo is

Personal site for [dan cargill](https://cargill.dev) — Next.js App Router, React, TypeScript, Tailwind, and shadcn/ui.

## Package manager & scripts

- Use `bun` (`bun install`, `bun run <script>`, `bunx`).
- Prefer existing `package.json` scripts over ad-hoc commands.
- Do not add dependencies without asking first.
- Before adding a dependency, check whether an existing dependency or built-in API can solve the problem.

Useful scripts:

- `bun run dev` — development server
- `bun run lint` — Next.js ESLint
- `bun run format` / `bun run format:check` — Prettier (`@dc_/prettier-config`)
- `bun run build` — production build

## Preferred libraries

For default library choices (styling, animation, schemas, forms, state, data fetching, UI, auth, URL state, icons, dates, charts, fake data, themes, captchas), follow [docs/PREFERRED_LIBRARIES.md](docs/PREFERRED_LIBRARIES.md).

Project overrides (existing deps win; do not swap them unless asked):

- Icons already use `lucide-react` — keep Lucide; do not add Phosphor.
- Env validation uses `@t3-oss/env-nextjs` + Zod (`src/env.ts`).
- UI primitives are shadcn/ui under `src/components/ui`.

## Stack & layout

- Next.js App Router under `src/app`
- Shared UI in `src/components`
- Helpers and data in `src/lib`
- Shared types in `src/types`
- Path alias: `@/*` → `src/*`

## Working style

- Inspect existing code before changing it.
- Prefer small, focused diffs.
- Match nearby patterns before introducing new ones.
- Do not make unrelated refactors while completing a task.
- Prefer server components by default; add `"use client"` only when needed.

## Git

- Work on a feature branch; do not commit directly to `main`.
- Use Conventional Commits: `type(scope): summary`.
- Do not add AI co-author footers to commits or PRs.
