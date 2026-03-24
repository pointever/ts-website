# Table Service — Marketing / legal site

Static site for **https://tableservice.app**: landing page, Terms of Service, Privacy Policy, and User Privacy Choices. Served separately from the Table Service app.

## Deploy (GitHub Pages)

1. Create a **new** GitHub repo (e.g. `pointever/ts-website` or `pointever/tableservice-website`) and push this folder as the repo root (e.g. clone the app repo, copy contents of `website-repo/` into a new repo, or add this folder as a separate remote and push).
2. In the new repo: **Settings → Pages** → set **Source** to **GitHub Actions**.
3. Under **Custom domain**, set `tableservice.app` and enforce HTTPS.
4. In your DNS for `tableservice.app`, add the CNAME or A records GitHub shows.
5. Push to `main`; the workflow deploys the site.

## Contents

- `index.html` — Home / splash
- `terms.html` — Terms of Service
- `privacy.html` — Privacy Policy
- `privacy-choices.html` — User privacy choices
- `app-icon.svg` — home page logo (matches iOS app icon artwork)
- `ts-logo.svg` — horizontal wordmark (optional / legacy URLs)
- `CNAME`, `.nojekyll`
