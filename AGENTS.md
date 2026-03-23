# Repository Guidelines

## Project Structure & Module Organization
This repository is a small Next.js 16 App Router project. Primary application code lives in `app/`: `layout.tsx` defines the root shell, `page.tsx` is the current home page, and `globals.css` holds shared Tailwind v4 styles. Static assets belong in `public/`. Product notes and MVP planning live in `docs/`, currently `docs/ai-expense-manager-mvp.md`. Use the `@/*` TypeScript path alias for imports from the repository root.

## Build, Test, and Development Commands
- `npm run dev`: start the local dev server at `http://localhost:3000`.
- `npm run build`: create a production build and catch compile-time issues.
- `npm run start`: run the built app locally after `npm run build`.
- `npm run lint`: run ESLint with the Next.js core-web-vitals and TypeScript rules.

## Coding Style & Naming Conventions
Use TypeScript with `strict` mode enabled. Follow the existing style: 2-space indentation, double quotes, and semicolons. Keep React components in PascalCase, route files in Next.js conventions (`page.tsx`, `layout.tsx`), and CSS custom properties in kebab-case. Prefer functional components and colocate route-specific UI inside `app/` until shared modules justify extraction. Run `npm run lint` before opening a PR.

## Testing Guidelines
There is no test runner configured yet. Until one is added, treat `npm run build` and `npm run lint` as the minimum verification step for every change. When tests are introduced, place them next to the feature or in a dedicated `__tests__/` directory and use `*.test.ts` or `*.test.tsx` naming.

## Commit & Pull Request Guidelines
Git history is not available in this workspace snapshot, so no existing commit pattern can be verified. Use short, imperative commit messages such as `feat: add dashboard shell` or `fix: correct metadata title`. PRs should include a concise summary, the user-facing impact, verification steps, and screenshots for UI changes. Link the relevant issue or planning note when applicable.

## Configuration & Content Notes
Do not commit secrets or local `.env*` files. Keep financial sample data anonymized. If product scope changes, update `docs/ai-expense-manager-mvp.md` alongside the implementation.
