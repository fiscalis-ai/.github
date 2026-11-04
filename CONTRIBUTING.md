# Contributing

## Workflow (trunk-based)
1. Create a short-lived branch from `main` (max 1–2 days): `feat/…`, `fix/…`, `chore/…`.
   Fork-based repos: create it in your fork.
2. Open a pull request. The **title** must be a [Conventional Commit](https://www.conventionalcommits.org):
   - `fix: …` → patch release
   - `feat: …` → minor release
   - `feat!: …` or `BREAKING CHANGE:` in the body → major release
   - `chore|docs|refactor|test|ci|build|perf: …` → no release
3. Squash-merge only after at least 1 approval and green `ci`, `pr-title` and `security` checks.
4. Hide unfinished work behind feature flags. `main` must always be deployable.

Violations are reported automatically as issues by the `guard` workflow.

## Releases
release-please keeps a `chore(main): release x.y.z` pull request open. Merging it creates the
tag, GitHub Release and changelog. Never create `v*` tags by hand; they are deleted.

## Local setup
Run `npx lefthook install` once after cloning. It checks commit messages and blocks pushes to `main`.
