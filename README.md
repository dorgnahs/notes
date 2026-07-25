# Portfolio Site — Monocle Editorial

A five-page site sharing one stylesheet: near-white paper, black ink, black
rules for structure, one yellow accent. Flat surfaces, no shadows, no
rounded corners — modeled on Monocle's masthead/rules and the NYT Arts
front's ruled columns. Pure HTML/CSS, no JavaScript, no build step.

## Pages
- `index.html` — home: hero + 3×2 grid linking into the site
- `work.html` — project index (ruled list, most recent first)
- `writing.html` — essay index (same list pattern)
- `about.html` — bio, two-column with a placeholder figure + fact list
- `contact.html` — commission process (3-step) + availability note

All five share the same `<header class="nav">` and `<footer class="footer">`
markup and load the same `style.css`.

## Customize
1. Replace "Maya Okafor" / `M·O` across all five files (and each `<title>`).
2. **Work/Writing:** duplicate an `.article-row` to add an entry; the meta
   column (year/category or date/tag) is the sort key, so keep entries in
   date order.
3. **About:** rewrite the three bio paragraphs and the `.fact-list` items.
   Swap the placeholder SVG in `.about-figure` for a real `<img>` — keep the
   container's 4:5 aspect ratio or adjust the CSS `aspect-ratio` to match.
4. **Contact:** edit the three `.process-list` steps and the availability line.
5. Retint via `:root` in `style.css` (`--paper`, `--ink`, `--accent`).
6. Nav links use `class="current"` on whichever page you're on, for the
   underline state — already wired on each page.

## Deploy on GitHub Pages
**Personal site:** repo named `<username>.github.io`, push all six files
(five `.html` + `style.css`) to `main`, visit `https://<username>.github.io`.

**Project site:** any repo → Settings → Pages → Deploy from a branch →
`main` / root → publishes at `https://<username>.github.io/<repo>/`.

Keep every file at the repo root (or update the relative links/`href`s if
you nest them in a folder). Only external dependency is Google Fonts.
