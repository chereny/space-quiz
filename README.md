# Orbit

A dependency-free space exploration quiz with ten questions, answer explanations,
live scoring, missed-answer review, and shareable results. The page supports
keyboard answers (keys **1-4**), light and dark color schemes, small screens, and
reduced-motion preferences.

**Website:** https://chereny.github.io/space-quiz/

## Run locally

Clone this repository and open `index.html` directly in a modern web browser.
No installation, build command, or development server is required. JavaScript
must be enabled.

All HTML, CSS, quiz data, and application logic live in `index.html`.

## Deployment

GitHub Pages uses **GitHub Actions** as its publishing source. The
[`Deploy GitHub Pages`](.github/workflows/pages.yml) workflow prepares and checks
the static site on pull requests targeting `main`. After a push or merge to
`main`, it publishes only `index.html` to GitHub Pages. No compilation is needed.

To redeploy manually, open **Actions > Deploy GitHub Pages > Run workflow** and
select `main`. Deployment status and logs are available in the workflow run and
the repository's `github-pages` environment.
