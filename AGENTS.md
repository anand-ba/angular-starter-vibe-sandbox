# AGENTS.md

## Cursor Cloud specific instructions

This is a **frontend-only** Angular 21 SPA ("My Vibe Coding Sandbox"). No backend, database, or external services are required.

### Key commands

See `README.md` "Available Scripts" table for the full list. Highlights:

| Task | Command |
|------|---------|
| Dev server | `npm run start` (port 4200) |
| Lint | `npm run lint` |
| Unit tests | `npm run test` |
| E2E tests | `npm run e2e` (requires Playwright browsers — run `npx playwright install --with-deps chromium` first) |
| Prod build | `npm run build:prod` |

### Non-obvious notes

- `.npmrc` sets `legacy-peer-deps=true`; do not remove it or `npm install` will fail on peer dependency conflicts.
- The `prepare` script runs `husky` on install to set up Git commit hooks (commitlint for conventional commits).
- Playwright browsers are **not** installed by `npm install`. If you need E2E tests, install them explicitly with `npx playwright install --with-deps chromium`.
- The production build emits a CSS `@import` ordering warning — this is pre-existing and harmless.
- Transloco i18n is configured but translation files (`src/assets/i18n/*.json`) are empty; the UI text is currently hardcoded.
