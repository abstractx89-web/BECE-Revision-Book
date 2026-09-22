# Revision Book — BECE Practice

A single-page study app for BECE past-question practice: pick a subject, pick
a year, choose timed or untimed, work through the questions, and review what
you struggled with. All 639 questions (2024 + 2025, all 8 subjects) are baked
into `index.html`, so once it's loaded once it keeps working offline.

## Files

- `index.html` — the whole app (HTML, CSS, JS, and all question data in one file)
- `sw.js` — a small service worker that caches the app so it opens offline after the first visit
- `README.md` — this file

## Put it on GitHub Pages

1. Create a new repository on GitHub (public or private both work for Pages on a paid plan; use **public** if you're on the free plan).
2. Upload `index.html` and `sw.js` to the root of that repository — drag-and-drop them in through the GitHub web UI, or:
   ```
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>
   # copy index.html and sw.js into this folder
   git add index.html sw.js
   git commit -m "Add Revision Book app"
   git push
   ```
3. In the repository, go to **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to "Deploy from a branch", pick the `main` branch and the `/ (root)` folder, then **Save**.
5. GitHub will publish it at:
   ```
   https://<your-username>.github.io/<repo-name>/
   ```
   This can take a minute or two the first time. Refresh the Pages settings page and the live link will appear there once it's ready.

## After that

- Open the link on your phone and use **Add to Home Screen** (Share button on iPhone, browser menu on Android) — it'll launch full-screen with its own icon, like an installed app.
- Scores and history are saved on each device separately (there's no shared account or server), and now persist reliably in every mobile browser, including Safari on iPhone.
- The first visit needs an internet connection; after that, the app works fully offline thanks to `sw.js`.

## Updating it later

When you get new year packs to add, send them back to me and I'll rebuild
`index.html` for you — just re-upload the new version to the same repo (same
filename, overwrite the old one) and GitHub Pages updates automatically
within a minute or two. `sw.js` won't usually need to change.
