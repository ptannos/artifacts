# Project Guidance

## Stack

- TypeScript 5 with strict type checking.
- React 19 and Next.js 16 App Router.
- Application code lives under `src/`; route files live in `src/app/`.
- Tailwind CSS 4 is configured through `@import "tailwindcss"` in `src/app/globals.css`.
- `next.config.ts` enables Cache Components and Partial Prefetching.

## Working in This Repository

- Before using or changing Next.js APIs, read the relevant guide in `node_modules/next/dist/docs/`. This project uses Next.js 16, whose conventions may differ from older versions.
- Keep route-specific files in the relevant `src/app/` segment. Put reusable UI in `src/components/` and shared non-UI logic in an appropriate `src/` module.
- Prefer Server Components. Add the `"use client"` directive only when a component needs browser APIs, state, effects, or event handlers; keep that boundary as small as practical.
- Follow the existing strict TypeScript configuration. Prefer explicit, useful types and avoid `any`.
- Follow the existing Tailwind CSS 4 setup and project styling conventions. Do not add a styling dependency without a concrete need.
- Treat server/client boundaries and secrets carefully: keep credentials and server-only work out of client modules, and validate untrusted input at the boundary where it enters the application.
- Preserve existing user changes and keep edits focused on the requested behavior.

## Validation

- Run `npm run lint` after changes.
- Run `npm run build` for changes that affect routes, rendering, configuration, or production behavior.
- There is currently no test script configured in `package.json`; do not assume a test suite exists.

## Commands

- `npm run dev` starts the development server.
- `npm run lint` runs ESLint.
- `npm run build` creates a production build.
- `npm run start` serves the production build.
