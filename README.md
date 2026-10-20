# mangapostcard-links

Link-in-bio page for @mangapostcard, served by GitHub Pages.

- `index.html` — static page; renders `series.json` in the browser (newest entry is shown as "Just posted").
- `series.json` — series list and the CDJapan affiliate base URL.
- `covers/` — volume 1 thumbnails (360px wide).

## Updating

Entries are added automatically by `python orchestrator.py reel-bookstore` in the private
`mangapostcard` project when `LINKS_SITE_DIR` points to this folder. Commit and push to publish.

Fields you can edit by hand in `series.json` (kept across re-runs):

- `set_product` — CDJapan complete-set product code (e.g. `NEODAI-130192`). When set, the main
  button links to that product page instead of a search.
- `search_query` — the term used for the CDJapan search links.
