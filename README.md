# eschmitt88.github.io

Personal landing page, served at <https://eschmitt88.github.io>.

Zero-build: plain `index.html` + `style.css`, no static-site generator.
The empty `.nojekyll` file tells GitHub Pages to serve files as-is and skip
the Jekyll build step.

## Self-updating project list

The "Live project sites" section is **not hand-maintained**. On load,
`index.html` makes one GitHub API call (`/users/eschmitt88/repos`), keeps the
public, non-fork repos with Pages enabled (`has_pages`), and links each to its
`https://eschmitt88.github.io/<repo>/` site, newest first. The list inside the
`<ul id="projects">` is only a static fallback shown if JS is off or the
unauthenticated API is rate-limited (60 req/hr/IP); JS replaces it when it loads.

So: to add a project to the landing page, just make its repo public and enable
Pages — no edit here is needed. A repo's card description comes from its GitHub
`description` field (set with `gh repo edit <repo> --description "…"`).

## Edit

Edit `index.html` / `style.css` and push to `main`. Pages redeploys
automatically (usually live within ~1 minute).
