# Jatin Singhi - Personal Website

Personal portfolio website for Jatin Singhi - 18-year-old entrepreneur, Founder @ Klay Education,
Head of Operations @ Project Clay.

## Design system

The site wears the **Klay design system**, vendored from `/Users/jj/klay code/site/src/styles`.
These files are **verbatim copies** - do not edit them here. Fix them upstream in the Klay repo and
re-copy, or the two will drift:

| File | Upstream |
|------|----------|
| `styles/tokens.css` | `site/src/styles/tokens.css` - the whole `--ga-*` token set |
| `styles/fonts.css`  | `site/src/styles/fonts.css` |
| `styles/base.css`   | `site/src/styles/base.css` |
| `styles/keys.css`   | `site/src/styles/keys.css` - the keycap button |
| `styles/card.css`   | `site/src/components/ui/Card.css` |
| `styles/pill.css`   | `site/src/components/ui/Pill.css` |

`styles/site.css` is the **only** stylesheet written for this site. It assembles the vendored
components into this page's shapes and adds the responsive rules (Klay's own `mobile.css` is
app-chrome specific and deliberately not vendored). It never redefines a token.

Fonts in `fonts/` are self-hosted and OFL-licensed - **Overused Grotesk** (350/400/500/600; there is
no 700, semibold is the ceiling) and **Departure Mono** (the pixel display face). The licence files
ship alongside them and must stay.

`images/klay-logo.svg` is the Klay Education pixel wordmark. The copy inlined in `index.html` uses
`fill="currentColor"` plus `shape-rendering="crispEdges"` so one copy inks correctly in both themes
without antialiasing the pixel grid.

## Theme

Light by default, `.dark` class on `<html>`, choice stored under `localStorage["jatin-theme"]`.
**Three values in `<head>` have to agree** - `<meta name="theme-color">`, `<meta name="color-scheme">`
and the `false` default in the pre-paint script. Change all three or none; a light page under a dark
browser bar is exactly the flash that script exists to prevent.

## Local Development

### Prerequisites

- [Node.js](https://nodejs.org/) (version 14 or higher)

### Setup Instructions

1. **Install dependencies**:
   ```bash
   npm install
   ```

2. **Start the development server**:
   ```bash
   npm start
   ```

   This will:
   - Start a local server on port 8080
   - Automatically open your browser to http://localhost:8080
   - Enable live reload (changes auto-refresh in browser)

3. **Alternative command**:
   ```bash
   npm run dev
   ```

### Troubleshooting

- **Port already in use**: If port 8080 is occupied, you can modify the port in [package.json](package.json) by changing the `--port=8080` value in the start script.
- **Browser doesn't open automatically**: Manually navigate to http://localhost:8080
- **Changes not reflecting**: Check the terminal for errors, or try stopping the server (Ctrl+C) and running `npm start` again.

## Quick Start (No Installation)

If you don't have Node.js installed, you can still view the site by opening `index.html` directly in your browser. However, you won't have live reload functionality.

