# Deploying the Portfolio

The site is fully static — `index.html` plus the `assets/` folder (project
images), no build step. Always deploy both together; images are referenced by
relative path (`assets/...`). Two easy options.

## Option A — GitHub Pages (recommended, free, custom URL later)

1. **Create the repo.** On GitHub, create a new public repo named
   `tchowdhury30.github.io` (this exact name gives you the root URL
   `https://tchowdhury30.github.io`). For a project page instead, any repo name
   works (e.g. `portfolio`) and the URL becomes
   `https://tchowdhury30.github.io/portfolio/`.

2. **Push this folder.** From `/Users/t/Documents/cs/portfolio/`:

   ```bash
   git init
   git add index.html DEPLOY.md assets/
   git commit -m "Portfolio site"
   git branch -M main
   git remote add origin https://github.com/tchowdhury30/tchowdhury30.github.io.git
   git push -u origin main
   ```

3. **Enable Pages.** On GitHub: repo → **Settings → Pages** → under
   "Build and deployment", set Source to **Deploy from a branch**, pick
   `main` / `/ (root)`, and save. The site is live at
   `https://tchowdhury30.github.io` within a minute or two. (For the
   `tchowdhury30.github.io` repo name, Pages is usually enabled automatically.)

## Option B — Netlify drag-and-drop (fastest, ~30 seconds)

1. Go to <https://app.netlify.com/drop> (sign in or create a free account).
2. Drag the entire `portfolio` folder from Finder onto the drop zone.
3. Done — Netlify gives you a live URL immediately. Rename it under
   **Site settings → Change site name** (e.g. `tasnimchowdhury.netlify.app`).

## Updating later

- **GitHub Pages:** edit `index.html`, then `git add -A && git commit -m "update" && git push`.
- **Netlify:** open your site's **Deploys** tab and drag the folder in again.
