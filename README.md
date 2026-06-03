# Lozano — Menu Website

A single-page, static restaurant menu for **Lozano — The Gourmet Awakening**.
No build step. The logo and favicon are embedded in `index.html`, so the only
required file to deploy is `index.html`.

## Features
- Branded hero with the Lozano logo, daily hours (8:00 AM – 12:00 PM) and a live
  "Open now / Closed" indicator.
- Live menu **search**.
- Sticky category navigation.
- A front-end **Staff editor** to change product names/prices, add or remove
  products, and add sections.

## Editing the menu (Staff editor)
1. Scroll to the footer and click **Staff Login**.
2. Sign in — username `areeh`, password `areeh123`.
3. Edit names, prices, descriptions; add/delete products or sections.
4. **Save draft** keeps the changes in your browser (preview only).
5. **Publish** downloads `menu-data.json`. Commit that file to the repo root and
   push — the live site loads `menu-data.json` and shows the changes to everyone.

> Security note: the login is front-end only (the password is in `index.html`,
> visible to anyone who views the source) and "Save draft" is per-browser. It's a
> convenience gate, not real protection. For true multi-user security and shared
> persistence, a server/database backend is required.

## Deploy on Vercel
Static site — no configuration needed.
1. Push to GitHub (below).
2. https://vercel.com/new → import **Lozano**.
3. Framework Preset: **Other** · Build Command: empty · Output Dir: empty.
4. **Deploy**.

## Push to GitHub
```bash
git init
git add .
git commit -m "Lozano menu site"
git branch -M main
git remote add origin https://github.com/creativenetworkmv/Lozano.git
git push -u origin main
```

## Files
- `index.html` — the site (logo + favicon embedded).
- `menu-data.json` — optional; created via the Publish button. Overrides the
  built-in menu when present.
- `logo.png`, `favicon.png` — source assets (not required by the site).
