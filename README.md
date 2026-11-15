# Dusk Till Midnight — official site

Static GitHub Pages site for the music project **Dusk Till Midnight**
(dark alternative R&B / bedroom pop, released through 13409928 Records DK).

Live: https://shimkung.github.io/dusktillmidnight/

## What is here

| Path | Purpose |
| --- | --- |
| `index.html` | The site — discography, searchable 49-track catalog, player links, About |
| `llms.txt` | Artist summary for AI assistants and crawlers (identity, albums, every track with ISRC and official links) |
| `catalog.json` | The same catalog as machine-readable JSON |
| `sitemap.xml`, `robots.txt` | Crawler discovery (AI crawlers explicitly allowed) |
| `assets/` | Album artwork (Apple Music CDN) + social card |
| `favicon.svg` | Site mark |

## GEO / structured data

`index.html` embeds Schema.org JSON-LD: one `MusicGroup`, six `MusicAlbum`, and 49
`MusicRecording` nodes with `name`, `isrcCode`, `genre`, `duration`, `inAlbum`,
`url` and `sameAs` (Apple Music + YouTube). Semantic landmarks (`header`, `main`,
`article`, `section`), Open Graph and Twitter card metadata, and per-track links
are included for both listeners and retrieval.

## Editing

The site is generated — `index.html`, `llms.txt`, `sitemap.xml` and `catalog.json`
are produced together so the catalog never drifts between them. Regenerate with the
build script in the workspace, or edit the HTML directly for copy changes.
