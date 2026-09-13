# Google Search Clone

A simple static clone of the Google homepage, built with HTML, CSS, and Bootstrap. It includes three pages that mimic Google's basic search, image search, and advanced search interfaces.

## Pages

- **`index.html`** — Search
  The main landing page with the Google logo, a search input, a "Google Search" button, and an "I'm Feeling Lucky" button (links to Google Doodles).

- **`image.html`** — Image Search
  Same layout as the main page, but submits with a hidden `udm=2` parameter to route the query to Google Image Search results.

- **`advanced.html`** — Advanced Search
  A form offering more specific query options:
  - All of these words (`as_q`)
  - Exact phrase or word (`as_epq`)
  - None of these words (`as_eq`)
  - Site or domain (`as_sitesearch`)

All three pages share the same top navigation bar for switching between Search, Image, and Advanced.

## How it works

Each page's `<form>` submits a GET request directly to `https://www.google.com/search`, passing along the appropriate query parameters (`q`, `udm`, `as_q`, `as_epq`, `as_eq`, `as_sitesearch`). No backend or JavaScript logic is required — search results are rendered by Google itself.

## Tech stack

- **HTML5** for page structure
- **Bootstrap 5.3.8** (via CDN) for the grid layout, dark theme (`bg-dark text-white`), and base styling
- Inline `style` attributes for the pill-shaped inputs/buttons and layout tweaks

## Project structure

```
.
├── index.html      # Main search page
├── image.html      # Image search page
└── advanced.html   # Advanced search page
```

## Running locally

No build step is needed. Simply open `index.html` in a browser, or serve the folder with any static file server, e.g.:

```bash
python3 -m http.server
```

Then visit `http://localhost:8000` in your browser.

## Notes

This project is for educational/demo purposes only and is not affiliated with or endorsed by Google.
