# nathanielthick.github.io

Personal portfolio for **Nathaniel Thickett**, Test Engineer & Software Developer.

**Live site:** https://nathanielthick.github.io/

It's a single page with selected projects, work experience, skills, an about section and contact links, plus a downloadable résumé. It's built by hand with plain HTML, CSS and a little JavaScript. There's no framework, no build step and no dependencies to install.

## Project structure

| Path | What it is |
| --- | --- |
| `index.html` | The whole page: content, icon sprite, SEO tags and JSON-LD |
| `assets/css/site.css` | All styles. Colors are CSS variables, with a dark theme |
| `assets/js/site.js` | Theme toggle, mobile menu, active nav link, scroll fade-ins, copy-email button |
| `assets/Nathaniel-Thickett-Resume.pdf` | The résumé linked from the page |
| `images/projects/` | Project screenshots (`.webp` with a `.jpg` fallback) |
| `images/og-card.png` | 1200×630 preview image for links shared on LinkedIn, Slack and other sites |
| `images/apple-touch-icon.png`, `favicon.svg` | Site icons |
| `404.html` | Custom "page not found" page |
| `robots.txt`, `sitemap.xml` | Search engine files |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |

## Run it locally

Any static file server works. With Python installed:

```powershell
python -m http.server 8123
```

Then open http://localhost:8123. Opening `index.html` directly also works, but the 404 page and some absolute paths need a server.

## Deploy

GitHub Pages serves the `main` branch. Push to `main` and the site updates within a minute or two.

## Updating content

- **Projects, jobs and skills** are plain HTML in `index.html`, one block per item. Copy a block that's already there to add a new one.
- **Résumé:** replace `assets/Nathaniel-Thickett-Resume.pdf` and keep the same file name, so every link keeps working.
- **After changing `site.css` or `site.js`:** bump the `?v=` date in `index.html` and `404.html` so browsers fetch the new file instead of a cached copy.
- **Job title or headline:** also update the `<title>`, the meta description, the Open Graph tags and the JSON-LD block at the top of `index.html`, then regenerate `images/og-card.png`.
- **`sitemap.xml`:** update `<lastmod>` after major content changes.

## Credits

Fonts: [Geist and Geist Mono](https://fonts.google.com/specimen/Geist), loaded from Google Fonts.
