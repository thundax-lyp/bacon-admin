# Repository Guidelines

## Project Structure & Module Organization
This repository is currently a minimal Node.js scaffold for the Bacon Admin UI.

- Root files: `package.json`, `package-lock.json`, `README.md`, `LICENSE`
- Documentation area: `docs/` (currently empty; add architecture notes, API contracts, and design decisions here)
- Application source: not yet created; place runtime code under `src/` and keep entry files explicit (for example, `src/index.js`)
- Tests: create a dedicated `test/` (or `tests/`) directory and mirror source paths where possible

## Build, Test, and Development Commands
Use npm for local workflows:

- `npm install`: install project dependencies from `package-lock.json`
- `npm test`: runs the configured test script in `package.json` (currently a placeholder and should be replaced when tests are added)
- `npm run <script>`: add scripts such as `dev`, `build`, and `lint` to standardize contributor workflows

Example script additions in `package.json`:
- `"dev": "node src/index.js"`
- `"lint": "eslint ."`
- `"test": "jest"`

## Coding Style & Naming Conventions
- JavaScript runtime is CommonJS (`"type": "commonjs"`); use `require`/`module.exports` unless the project explicitly migrates
- Use 2-space indentation and keep lines readable (prefer <= 100 chars)
- File naming: kebab-case for files (`user-service.js`), PascalCase for React components if added (`UserTable.jsx`)
- Keep modules focused; avoid large multi-purpose files
- If ESLint/Prettier are added, run them before opening a PR

## Testing Guidelines
- Adopt a single framework (recommended: Jest) and wire it to `npm test`
- Test files should end with `.test.js` and sit beside modules or under `tests/`
- Cover new logic with unit tests and include regression tests for bug fixes

## Commit & Pull Request Guidelines
- Current history uses short, imperative commits (for example, `Initial commit`); continue with concise subject lines
- Prefer format: `<type>: <summary>` (for example, `feat: add user list page`, `fix: handle empty response`)
- PRs should include: purpose, key changes, test evidence (`npm test` output), and linked issue(s)
- Include screenshots or short recordings for UI changes
