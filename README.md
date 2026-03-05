# arXiv Scout

A daily arXiv paper scanner that filters new astro-ph submissions by customizable keyword groups, with instant search and shareable configurations.

## Features

- **New submissions only** — automatically filters out replacements and cross-listings
- **Keyword group matching** — papers are organized into configurable groups (Galaxy Evolution, Dwarf Galaxies, Low Surface Brightness, Dark Matter)
- **Keyword highlighting** — matched terms are highlighted in titles and abstracts
- **Instant search** — filter results by title, abstract, or author
- **Date range mode** — fetch papers from a custom date range via the arXiv API
- **Shareable configs** — keyword configurations are encoded in the URL hash, so you can bookmark or share your setup
- **Zero dependencies** — single HTML file, no backend, no build step

## Usage

### Online

Visit the live app: [https://shanyDanieli.github.io/arxiv-scout/](https://shanyDanieli.github.io/arxiv-scout/)

### Local

Download `index.html` and open it in any modern browser. That's it.

### Customizing Keywords

1. Click the **⚙ Keywords** button in the header
2. Edit, add, or remove keyword groups
3. Click **Save & Reload**
4. Use the **🔗 Share** button to copy a URL with your custom configuration

## How It Works

The app fetches the daily new submissions listing from [arxiv.org/list/astro-ph/new](https://arxiv.org/list/astro-ph/new) via a CORS proxy, parses the HTML to extract paper metadata, and matches papers against your keyword groups using word-boundary matching. No server required — everything runs client-side in your browser.

## Deployment

### GitHub Pages

1. Fork or clone this repo
2. Go to **Settings → Pages → Source** → select `main` branch
3. Your app will be live at `https://shanyDanieli.github.io/arxiv-scout/`

### Self-hosted

Copy `index.html` to any web server's public directory. No build step or server-side runtime needed.

## License

MIT
