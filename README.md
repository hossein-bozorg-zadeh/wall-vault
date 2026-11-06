# WallVault 🌌

A single-file wallpaper web app — high-resolution backgrounds gathered from
multiple internet sources, with search, categories, colors, favorites,
lock-screen preview and 4K downloads. No server, no build step, no database.

## Run it

Just open `index.html` in a browser, or serve the folder:

```bash
npx serve .          # or: python3 -m http.server 8746
```

## Put it on GitHub Pages (free hosting)

1. Create a new repository on GitHub (e.g. `wall-vault`).
2. Run these commands in this folder:

```bash
git init
git add index.html README.md
git commit -m "WallVault v1"
git branch -M main
git remote add origin https://github.com/YOURNAME/wall-vault.git
git push -u origin main
```

3. In the repo: **Settings → Pages → Source: Deploy from a branch → `main` / root → Save**.
4. Your app is live in a minute at `https://YOURNAME.github.io/wall-vault/`.

## Sources

| Source | Key needed | What it gives |
|---|---|---|
| WallWidgy API | none | 8 curated categories, color filters, phone/desktop crops |
| Lorem Picsum | none | real photography, crops to any resolution |
| Wikimedia Commons | none | searchable archive at full resolution |
| Openverse | none | web-wide open image index (search) |
| Paste-a-link | none | Pinterest/any direct image URL → becomes a wallpaper |
| Pexels *(optional)* | free key | huge searchable library, 4K originals |
| Unsplash *(optional)* | free key | huge searchable library + color filters |

Free keys: [pexels.com/api](https://www.pexels.com/api/) ·
[unsplash.com/developers](https://unsplash.com/developers) — paste them in
⚙️ Settings. Keys are stored only in your own browser (localStorage).

### Pinterest note
Pinterest blocks browsers from calling its API. Import pins by opening a pin,
right-clicking the image → **Copy image address** → ⚙️ Settings → paste under
“Pinterest & direct links”.

## Features

- 🔎 Instant search (Enter) across every active source
- 🗂 Category chips + color filters + Desktop/Phone layout switch
- ♾ Infinite scroll + “Load more” + deduped multi-source results
- ♥ Favorites saved in your browser (`#/favorites` route too)
- ⬇ Crop-to-resolution downloads: 4K / QHD / FHD / 1440×3120 / 1080×2340…
- 🖼 Lock-screen test: phone/monitor/laptop frame, drag + pinch/zoom, export your exact crop as an image
- 🎨 Dominant-color detection per wallpaper
- 🎲 “Surprise me” random wallpaper in one click
- 🌓 Dark / light theme, fully responsive mobile ⇄ desktop layout

## Files

- `index.html` — the entire app (HTML + CSS + JS in one file)
