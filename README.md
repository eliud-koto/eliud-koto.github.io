# eliud-koto.github.io

Personal academic website of Eliud Koto, served by GitHub Pages at
<https://eliud-koto.github.io/>.

Plain HTML, CSS and a few lines of JavaScript. No build step, no framework.

## Structure

```
index.html            single-page site (all sections)
blog/index.html       the blog index: standing note + list of posts
blog/_template.html   post template (not linked; copy it to start a post)
css/style.css         styles
js/main.js            mobile navigation toggle, footer year
assets/Eliud_Koto_CV.pdf   the CV linked from the site
assets/blog/          images used in posts
assets/favicon.svg
.nojekyll             tells GitHub Pages to serve files as-is
```

## Adding / updating the CV

The site links to `assets/Eliud_Koto_CV.pdf`. That file is **not** committed
yet: place a public-safe PDF (no referee contact details) at exactly that path,
then commit and push. The "View CV" and "Download CV" links will work as soon
as it is there. To update later, replace the file (keep the name) and push again.

## Adding a post

1. Copy `blog/_template.html` to `blog/<slug>.html`.
2. Replace the placeholders: `<title>`, description, canonical URL, `<h1>`,
   the `<time>` element, and the body. Delete the template notice.
3. Add an entry to the `.post-list` in `blog/index.html`, newest first:

```html
<li>
  <p class="post-date"><time datetime="2026-09-23">23 September 2026</time></p>
  <h3><a href="my-slug.html">The post title</a></h3>
  <p>One sentence on what the post is about.</p>
</li>
```

4. Mirror the newest two entries in the Blog section of `index.html`, and
   remove the `post-list-empty` placeholder from both lists once real posts exist.

## Editing content

All content lives in `index.html`. Each section has an `id` that matches the
navigation (`#about`, `#research`, `#publications`, `#projects`, `#experience`,
`#education`, `#cv`, `#blog`, `#contact`).

## Local preview

Open `index.html` directly in a browser, or from this directory:

```
python -m http.server 8000
```

and visit <http://localhost:8000/>.
