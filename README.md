# Gogotan, LLC — Reference Website

**Version:** 1.0 · **Date:** 2026-07-19

A minimal, static reference page for Gogotan, LLC, built for GitHub Pages. Informational only — no marketing, no lead capture, no analytics, no external requests, no build step.

## Files

| File | Purpose |
|---|---|
| `index.html` | The complete site (HTML + inline CSS, self-contained) |
| `404.html` | Branded "page not found" page linking back to home |
| `.nojekyll` | Tells GitHub Pages to serve files as-is (skips Jekyll processing) |
| `README.md` | This file |

## Deploy to GitHub Pages (publish from a branch)

These steps were verified against the current GitHub Pages settings UI as of July 2026.

1. Create a **public** GitHub repository.
   - For a site at `https://<username>.github.io/`, name the repo exactly `<username>.github.io`.
   - For a project site at `https://<username>.github.io/<repo>/`, any repo name works.
2. Add `index.html`, `.nojekyll`, `404.html`, and `README.md` at the **repository root** and push to the `main` branch.
3. In the repo, go to **Settings → Pages** (under the "Code and automation" section of the sidebar). Under **Build and deployment**:
   - **Source:** select **"Deploy from a branch."**
   - **Branch:** select `main`, folder `/ (root)`. Click **Save**.
4. Wait a few minutes. The live URL appears at the top of the Pages settings once the site deploys. Check **Enforce HTTPS** on the same page.
5. Troubleshooting if the site 404s:
   - The repo must be **public** (for free accounts).
   - `index.html` must be at the top level of the published folder.
   - The push must come from someone with admin permissions and a verified email address.
   - Check the **Actions** tab for the `pages-build-deployment` run status.
   - If the "Deploy from a branch" option is disabled, check **Settings → Environments → github-pages** for deployment branch restrictions.

A custom GitHub Actions workflow is available as an alternative publishing source but is unnecessary for a single static page.

**Project-site note:** all links in this site are relative or root-level, and the site is single-file, so it works at both root and project-site paths. The `404.html` home link points to `/`; on a project site, GitHub still serves the custom 404 but the link resolves to the account root — edit it to `/<repo>/` if you deploy as a project site.

## Version history

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-07-19 | Initial release. |
