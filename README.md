# Gray Zone Warfare Hideout Tracker

A static, browser-based hideout tracker. Includes inventory, sequential upgrades, automatic material deduction with Undo, a loot checklist, surplus items, and JSON backup import/export.

No installation, API keys, backend, or build step required. HTML, CSS and JavaScript files run directly on GitHub Pages. Typography uses Google Fonts, with system fallbacks when unavailable.

## Publish on GitHub Pages

1. Create a GitHub repository (a public repository works with GitHub Free).
2. Upload the CONTENTS of this folder to the repository root. `index.html`, `style.css`, `app.js`, and `data.json` must be alongside each other. Include `.nojekyll` if using Git; GitHub's file uploader may omit hidden files, but it is optional for this app.
3. Commit the files to `main`.
4. Open the repository's **Settings → Pages**.
5. Under **Build and deployment**, select **Deploy from a branch**.
6. Select **main** and **/(root)**, then **Save**.
7. GitHub will display the published URL when deployment completes. For a project repository it normally looks like `https://USERNAME.github.io/REPOSITORY/`.

Official instructions: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

Relative asset paths support project repositories and custom domains. No path configuration is necessary.

## Carry over your latest progress

1. On your existing tracker, click **Export backup** before switching sites.
2. Open your new GitHub Pages site.
3. Click **Import** and choose the downloaded JSON backup.
4. Confirm the replacement, then check your inventory and completed levels.

Progress does not transfer automatically between domains or browser profiles. The app uses the existing `gzw-hideout-v1` browser storage key and backup format, so previous backups remain compatible. Subsequent updates at the same address preserve saved data. Each visitor has their own browser-local inventory and progress; there is no shared account or cloud sync.

Export regular backups, especially before clearing browser data or changing browsers/domains. Do not upload your personal inventory backups to the repository; they are not required to run the site.

## Preview locally (optional)

From this folder, run `python3 -m http.server 8000`, then visit `http://localhost:8000`.

Use an HTTP server instead of double-clicking index.html: the browser fetches the requirements from data.json.

## Update

Edit and commit the site files on `main`; GitHub Pages republishes them. Keep index.html, style.css, app.js, and data.json together. Keep the storage key and backup format compatible to retain existing progress.

Requirements were transcribed from a user-supplied image, not verified against the current game version. Surplus calculations cover unfinished hideout upgrades only, not quests or other uses. Unofficial fan tool.

## Inventory images

Inventory tiles are sourced from [GZW Wiki](https://gzwiki.org/en/items), with per-item source links in the `icons` field of `data.json`. Game artwork belongs to its respective owners. Items without a verified tile display by name.

When publishing, include the `icons/` folder alongside the existing site files.
