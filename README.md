# release-tagging test bed

This repo is configured with [Release Please](https://github.com/googleapis/release-please) using the `simple` release strategy.

## Included setup

- `release-please-config.json`: Release Please configuration
- `.release-please-manifest.json`: Current tracked version (starts at `0.1.0`)
- `.github/workflows/release-please.yml`: GitHub Actions workflow that runs on pushes to `main`

## How it works

1. Push conventional commits to `main` (for example: `feat: add X`, `fix: correct Y`).
2. Release Please opens or updates a release PR.
3. Merge that release PR.
4. Release Please creates a GitHub Release and tag (for example `v0.2.0`).

## Quick test

Use a commit like:

```bash
git commit -m "feat: add initial release-please smoke test"
```

Then push to `main` and check the Actions tab for `Release Please`.
