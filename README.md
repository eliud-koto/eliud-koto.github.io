# eliud-koto.github.io

Personal academic website of Eliud Koto, served by GitHub Pages at
<https://eliud-koto.github.io/>.

Plain HTML, CSS and a few lines of JavaScript. No build step, no framework.

## Structure

```
index.html            single-page site (all sections)
css/style.css         styles
js/main.js            mobile navigation toggle, footer year
assets/Eliud_Koto_CV.pdf   the CV linked from the site
assets/favicon.svg
.nojekyll             tells GitHub Pages to serve files as-is
```

## Adding / updating the CV

The site links to `assets/Eliud_Koto_CV.pdf`. That file is **not** committed
yet: place a public-safe PDF (no referee contact details) at exactly that path,
then commit and push. The "View CV" and "Download CV" links will work as soon
as it is there. To update later, replace the file (keep the name) and push again.

## Editing content

All content lives in `index.html`. Each section has an `id` that matches the
navigation (`#about`, `#research`, `#publications`, `#projects`, `#experience`,
`#education`, `#cv`, `#contact`).

## Local preview

Open `index.html` directly in a browser, or from this directory:

```
python -m http.server 8000
```

and visit <http://localhost:8000/>.
