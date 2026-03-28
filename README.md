# Table Service — Marketing / legal website (`tableservice.app`)

This folder is the **standalone website** for **https://tableservice.app**. It is **not** the iOS/Android app and **not** the Angular/Capacitor UI (`src/` in the main repo).

## What to edit here

| You want to change… | Edit here |
|---------------------|-----------|
| App Store badge, link, hero copy on the **public website** | **`website-repo/`** (e.g. `index.html`, `download-on-the-app-store-white.svg`) |
| Terms / Privacy / Privacy Choices pages for **tableservice.app** | **`website-repo/`** (`terms.html`, `privacy.html`, `privacy-choices.html`) |
| The **mobile app** UI (screens, Account, etc.) | Main repo **`src/`** — not this folder |

**App Store badge + link:** Use the official white badge asset and point to your App Store URL (e.g. `https://apple.co/48fxXFE`) in **`index.html`** only under this folder for the static site.

## Deploy

This directory is meant to be the **root of its own GitHub repo** (e.g. **pointever/ts-website**) and deployed with **Cloudflare Pages** (or GitHub Pages). See **`../docs/WEB_SITE_BUILD_GUIDE.md`** in the main Table Service repo.

After you change files here, push to the **website** repo’s `main` branch so Cloudflare (or your host) rebuilds.

## `server/public/` in the main repo (optional mirror)

If **tableservice.app** is served by the **Node API on Railway** instead of (or in addition to) Pages, the same static files are kept under **`server/public/`** in the main repo so Express can serve them. When you update the marketing site, update **`website-repo/`** first, then copy the changed files to **`server/public/`** if you rely on Railway for the domain—or use only one hosting path and ignore the other.

## Contents

- `index.html` — Home (hero, App Store badge, legal nav)
- `terms.html`, `privacy.html`, `privacy-choices.html`
- `download-on-the-app-store-white.svg` — App Store Marketing badge (white)
- `app-icon.svg` — Home logo
- `ts-logo.svg` — Wordmark (optional)
- `CNAME`, `.nojekyll`, `.github/workflows/…`

**Legal copy:** Keep terms/privacy in sync with **`docs/web/`** in the main repo when wording changes.
