# .github

Organization-wide defaults for `fiscalis-ai`. This repository is public, so it must never contain secrets.

- Community health files: `CONTRIBUTING.md`, `SECURITY.md`, PR and issue templates.
- Reusable workflows in `.github/workflows/`, called as `fiscalis-ai/.github/.github/workflows/<name>.yml@v1`.
- Workflow templates in `workflow-templates/` (Actions → New workflow → "By fiscalis-ai").

Repositories calling `release.yml` or `request-review.yml` need the secrets `RELEASE_APP_CLIENT_ID` and
`RELEASE_APP_KEY`. `request-review.yml` also needs the organization permission **Members: Read-only** on the release app.