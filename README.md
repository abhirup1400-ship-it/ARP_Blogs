# ARP Blogs — Website

A single-page website for ARP Blogs featuring two book showcases, *One Love* and
*Unknown Strangers to Known Strangers (Book One — Chapter One)*. Visitors can read
each book online or download it as a PDF, any number of times.

The site is a single static `index.html` file with no build step and no
dependencies, so it can be hosted anywhere that serves static files —
including GitHub Pages, for free.

## What's in here

- `index.html` — the entire website. Both book PDFs are embedded inside this file,
  so the download and "Read Online" buttons work even if nothing else is uploaded.
- `One-Love-ARP-Blogs.pdf` — the *One Love* book (also kept as a standalone file).
- `Unknown-Strangers-to-Known-Strangers-Chapter-1.pdf` — Book One, Chapter One
  (also kept as a standalone file).
- `.nojekyll` — tells GitHub Pages to serve the files exactly as they are.
- `LICENSE` — copyright notice for the books.

Because the PDFs are embedded in `index.html`, the standalone `.pdf` files are
optional. They're included so you can link to them directly if you ever want to.

## Deploy to GitHub Pages

### Option A — Upload through the GitHub website (no command line)

1. Go to https://github.com/new and create a new repository (for example,
   `arp-blogs-website`). Leave it empty (no README) and make it Public.
2. On the new repo page, click **uploading an existing file**.
3. Drag in every file from this folder: `index.html`, both `.pdf` files,
   `.nojekyll`, `LICENSE`, and `README.md`. Click **Commit changes**.
4. Go to **Settings → Pages**.
5. Under **Build and deployment**, set **Source** to **Deploy from a branch**,
   choose branch **main** and folder **/ (root)**, then click **Save**.
6. Wait about a minute. Your site will be live at
   `https://YOUR-USERNAME.github.io/arp-blogs-website/`.

### Option B — Push with Git (command line)

This folder is already a git repository with one commit on the `main` branch.
After creating an empty repository on GitHub, run these commands from inside this
folder, replacing the URL with your own repository's URL:

```bash
git remote add origin https://github.com/YOUR-USERNAME/arp-blogs-website.git
git push -u origin main
```

Then enable Pages under **Settings → Pages** as described in steps 4–6 above.

### Tip — a site at your root domain

If you name the repository exactly `YOUR-USERNAME.github.io`, GitHub serves it at
`https://YOUR-USERNAME.github.io/` (no subfolder). Everything else works the same.

## Updating the site later

Edit `index.html` (or replace the PDFs), commit, and push again:

```bash
git add .
git commit -m "Update site"
git push
```

GitHub Pages redeploys automatically within a minute or two.

## Notes

- `index.html` is around 1.8 MB because both books are embedded inside it. This is
  well within GitHub's limits and loads quickly; the first visit may take a moment
  longer on slow connections.
- No analytics, ads, or trackers are included.
