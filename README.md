# Rosaschi website

The official website for Rosaschi, a skincare brand focused on high-performance eye care.

## Tech stack

- HTML5
- CSS3
- Vanilla JavaScript
- Formspree
- GitHub Pages

## Pages

- `index.html` — Home page and product overview
- `contact.html` — Contact form powered by Formspree
- `privacy.html` — Privacy policy
- `terms.html` — Terms of service
- `thank-you.html` — Form submission confirmation page

Shared styles live in `styles.css`. Brand imagery, fonts, and icons are stored under `assets/`, while browser and device icons are in `favicon/`.

## Run locally

From the repository root, serve the site with Python:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000/>.

Opening `index.html` directly may also work, but serving the directory is preferred because navigation, asset paths, and browser behavior more closely match production.

## Formatting

The repository includes Prettier configuration for consistent HTML and CSS formatting. With Node.js installed, run:

```sh
npx prettier --write "*.html" "*.css"
```

## Forms

The contact form submits through Formspree and displays an inline confirmation message after a successful submission. Its endpoint and form ID are configured in `contact.html`.

The early-access form on the home page is currently disabled. Connect it to an email provider and remove the disabled state only when signups are ready to open.

## Deployment

The repository root is deployed directly as a static site. No build command or output directory is required. The `CNAME` file configures `rosaschi.com` for GitHub Pages.
