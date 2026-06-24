# Maintaining the site

## To change a moon photo, a PDF, or any text — the easy way (hosted site)

Your GitHub-hosted site loads each moon photo straight from the `images/` folder and each
PDF from the `files/` folder. So to swap one:

1. Replace the file in `images/` (e.g. `images/titan.jpg`) or `files/` (e.g. `files/cv.pdf`),
   keeping the **same filename**.
2. Commit and push. That's it — no rebuild needed.

Keep photos at a reasonable size (long edge ~1000px) so pages load fast.

Moon → filename: `iapetus`, `titan`, `rhea`, `dione`, `tethys`, `enceladus`, `mimas`
(any of `.jpg` / `.png` / `.webp`).

To edit **text, links, captions, framing**, edit the `moonsData` list inside
`Saturn Orrery.dc.html`, then commit.

## To refresh the offline single-file (`Erin Flowers - Astrophysicist.html`)

That one file has everything baked in, so it must be rebuilt when assets change. Open
`build/rebuild.html` in your browser, select your images + PDFs + `Saturn Orrery.dc.html`
+ `support.js`, and click **Build**. It downloads a fresh `moon-assets.js` and
`Erin Flowers - Astrophysicist.html`. Nothing leaves your machine (it only fetches the
React runtime from unpkg, like the site does).

You only need this file if you share the site as a single downloadable/offline file. If you
deploy the multi-file set to GitHub Pages, you never have to rebuild anything — just swap
files and commit.
