# nineteenth-hole.github.io

The course catalogue for a home golf simulator in a Delhi basement.
One page, static HTML, no build step, no dependencies.

```
index.html          The Course Book — the whole catalogue
course-images/      one photograph per course (143)
```

## Publishing

This is a GitHub **organisation page**, so the org and the repository must both be called
`nineteenth-hole.github.io`:

1. Create an organisation named **nineteenth-hole**
2. Create a public repository inside it named **nineteenth-hole.github.io**
3. Push the contents of this folder to `main`
4. Settings → Pages → Deploy from a branch → `main` / `(root)`

Live at **https://nineteenth-hole.github.io**. Anyone with the link can read it.

## Updating

The data lives in `../courses.json`, which is the single source — rebuild the page from it,
never the other way round. After changing it, replace the one line in `index.html` that begins
`const COURSES = ` with the new array. Every image the data references must exist in
`course-images/`.

**If a group is renamed in the data, grep `index.html` for the old name** — the `GLOSS` and
`TURN` lookups are keyed on the same strings and fail silently when they drift.

## Later

Records (scores, the house championship) and Numbers (carry by club, dispersion) will want a
front page above the catalogue when there is data behind them. Until then the catalogue is the
site.
