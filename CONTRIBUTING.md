# Contributing

Thanks for taking the time to contribute! These guidelines apply to every repository under
[@bahriy-dev](https://github.com/bahriy-dev) unless a repository has its own `CONTRIBUTING.md`.

## Before you start

- **Bugs:** search the existing issues first, then open a bug report with steps to reproduce.
- **Features:** open a feature request before writing code, so we can agree on the approach.
- **Security problems:** do not open a public issue. See [SECURITY.md](SECURITY.md).

## Development workflow

1. Fork the repository and create a branch from `main`:
   `feat/short-description`, `fix/short-description` or `docs/short-description`.
2. Install and run the tests. Most projects only need:
   ```bash
   npm install   # skip for zero-dependency projects
   npm test
   ```
3. Keep the change focused. One pull request should solve one problem.
4. Add or update tests for any behaviour you change. Pull requests without tests for new
   behaviour will usually get a request for changes.
5. Update the README when you change public behaviour, configuration or endpoints.

## Commit messages

We use [Conventional Commits](https://www.conventionalcommits.org/):

```
feat: add discount coupons
fix: keep stock correct when an order is cancelled
docs: document the webhook routing config
test: cover expired coupons
chore: bump GitHub Actions
```

## Pull requests

- Fill in the pull request template.
- Link the issue it closes (`Closes #12`).
- Make sure CI is green. Type-checking runs in CI, so `npm run typecheck` locally saves a round trip.
- Pull requests are squash-merged, so the PR title becomes the commit message on `main`.

## Code style

- TypeScript in strict mode, no `any` in source code.
- Money is stored as integer kuruş, never floats.
- Prefer the platform (`node:http`, `node:crypto`, Web APIs) over new dependencies. If you do
  need a dependency, explain why in the pull request.

By contributing you agree that your contributions are licensed under the repository's license
and that you follow the [Code of Conduct](CODE_OF_CONDUCT.md).
