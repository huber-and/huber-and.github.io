# huber-and.github.io

The entry page for <https://huber-and.github.io/>.

GitHub serves a *user* Pages site from a repository named exactly `<username>.github.io`, at the
root of the domain. Project Pages — such as the documentation of
[atlassian-tools](https://github.com/huber-and/atlassian-tools) — are served from their own
repository under `/<repository>/` and are unaffected by this one.

| URL | Served from |
| :--- | :--- |
| `https://huber-and.github.io/` | this repository |
| `https://huber-and.github.io/atlassian-tools/` | `huber-and/atlassian-tools` |

## Structure

Plain static HTML, no build step and no external requests — no CDN fonts, no badge images, no
analytics. A visit loads exactly one file.

- `index.html` — the whole page, styles inlined, light and dark via `prefers-color-scheme`
- `.nojekyll` — skips Jekyll processing, so the file is served verbatim

## Setup

Once, after pushing this repository:

*Settings → Pages → Build and deployment → Source* = **Deploy from a branch**, branch `main`,
folder `/ (root)`.

No workflow is needed; GitHub publishes the branch content directly.

## Adding a project

Copy one `<article class="card">` block in `index.html` and adjust it. The layout is a single
column, so any number of cards works without touching the CSS.
