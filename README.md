# notebook-site

The published, public counterpart to a private personal notebook. Built with
[Jekyll](https://jekyllrb.com/) and the [Just the Docs](https://just-the-docs.com/)
theme, deployed via GitHub Pages (GitHub Actions build — see
[`.github/workflows/deploy.yml`](.github/workflows/deploy.yml)).

**Don't hand-edit files under `politics/`** (aside from `politics/index.md`) —
they're generated from the private notebook repo by
`scripts/sync-politics.ps1` over there. Edit the source note, re-run the
script, then commit and push here.

## First-time setup

1. Create this repo on GitHub as **public** (required for free GitHub Pages).
2. Push this folder to it.
3. In **Settings → Pages**, set **Source** to **GitHub Actions**.
4. In [`_config.yml`](_config.yml), replace `YOUR-GITHUB-USERNAME` in `url`,
   and update `baseurl` if you rename the repo.
5. Push to `main` — the "Deploy Jekyll site to Pages" workflow builds and
   publishes the site automatically.

## Local preview (optional)

```bash
bundle install
bundle exec jekyll serve
```
