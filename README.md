# CharlieKoch

A friendly, SEO-optimized static blog website for **Charlie Koch — President of Bank Midwest**, focused on Kansas City business, community banking, and local growth.

Live at: https://kansas-city.github.io/charlie-koch/ (GitHub Pages)

## What's inside

- **Home page** (`index.html`) — friendly hero, stats, latest posts, author intro, and calls to action
- **Blog** (`blog.html`) — all 10 articles with a sidebar
- **10 full articles** (`posts/`) — Kansas City business topics, including a feature on Kansas City Web Design Pros
- **About** (`about.html`), **Contact** (`contact.html`), **404** (`404.html`)
- **SEO built in**: unique titles/meta descriptions, canonical URLs, Open Graph + Twitter cards, `sitemap.xml`, `robots.txt`
- **Auto schema markup**: JSON-LD on every page — `WebSite` + `Person` (sitewide), `BlogPosting` + `BreadcrumbList` (articles), `CollectionPage` (blog), `AboutPage` / `ContactPage`
- Responsive design, mobile nav, semantic HTML5, accessible skip links — no build step, no dependencies

## Local preview

Just open `index.html` in a browser, or serve the folder:

```bash
python -m http.server 8000
```

Then visit http://localhost:8000

## Deploying to GitHub Pages

1. Push this folder to the `main` branch of the repository.
2. In the repo, go to **Settings → Pages → Build and deployment**.
3. Set **Source** to `Deploy from a branch`, choose branch `main` and folder `/ (root)`, then **Save**.
4. The site goes live at https://kansas-city.github.io/charlie-koch/ within a couple of minutes.

### Using a custom domain later

1. Add a `CNAME` file containing your domain (e.g. `charliekoch.com`).
2. Update all canonical/OG URLs (currently `https://kansas-city.github.io/charlie-koch/`) and the sitemap URLs to the new domain — a simple find-and-replace across the HTML files and `sitemap.xml`.

## Structure

```
├── index.html            # Home
├── blog.html             # Blog index
├── about.html            # About Charlie Koch
├── contact.html          # Contact
├── 404.html
├── posts/                # 10 articles
├── css/style.css
├── js/main.js
├── images/               # SVG logo, avatar, skyline, OG image
├── sitemap.xml
├── robots.txt
└── favicon.svg
```

## Note on images

- **Avatar**: Charlie Koch's photo (`images/charlie-koch.webp` / `.jpg`, plus a 400px variant) is used site-wide as the author avatar, in square crop at 800px and compressed to WebP.
- **Feature images**: each of the 10 articles has a topic-matched photo from [Unsplash](https://unsplash.com/license) (`images/feature-*.webp` with `.jpg` fallbacks), used as the card cover and article banner.
- **Social images**: per-post 1200×630 OG images (`images/og-<post>.jpg`) plus a branded default (`images/og-default.jpg`) for the home, blog, about, and contact pages.
- All photos are served as WebP with JPG fallback via `<picture>`. Replace the files in `images/` if you later want to use your own photography — filenames must stay the same.
