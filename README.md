# Mapped Assembly landing page

A buildless, responsive website for Mapped Assembly. The main site uses plain HTML and CSS; no dependencies, analytics, or external fonts. The legacy URL redirect uses a small script to preserve query strings and section anchors, with an HTML refresh and link fallback.

## Preview locally

From the repository root:

```bash
python3 -m http.server 8000
```

Open http://localhost:8000. Stop with Ctrl+C.

## Publish on GitHub Pages

The repository is [Mapped-Assembly/mapped-assembly.github.io](https://github.com/Mapped-Assembly/mapped-assembly.github.io). In **Settings → Pages**, the publishing source is **Deploy from a branch**, **main**, **/ (root)**. GitHub's managed `pages-build-deployment` workflow deploys pushes to `main`; no custom build workflow or compilation step is needed. `.nojekyll` keeps the files served as plain static assets.

The organization site is published at:

https://mapped-assembly.github.io/

Asset paths are relative to the root page. Canonical and Open Graph URLs point to the organization root. Keep the repository name `mapped-assembly.github.io` to retain this root address.

For an existing clone of the renamed repository, update its remote:

```bash
git remote set-url origin https://github.com/Mapped-Assembly/mapped-assembly.github.io.git
```

The former https://mapped-assembly.github.io/landing-page/ address is retained through `landing-page/index.html`. GitHub's repository rename does not redirect the old Pages URL automatically. This compatibility page performs a browser redirect to the root (HTTP 200 with JavaScript/HTML refresh, not a server-side 301). JavaScript preserves query strings and section anchors; the no-JavaScript fallback opens the root page.

See [GitHub's publishing source documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

## Content and evidence

Product descriptions were checked against the canonical README files on October 20, 2026:

- https://github.com/Mapped-Assembly/forma-oss
- https://github.com/Mapped-Assembly/Open-Industries
- https://github.com/Mapped-Assembly/CleanRoomOS

CleanRoomOS recognition refers to the September 27, 2026 NYC AI Nexus Build Day. SSI's LinkedIn company updates name Colara, CleanroomOS, and MedComm and call them winning concepts. The page says “one of the winning projects,” without claiming a sole first place, funding, or a commercial deployment.

- Team announcement: https://www.linkedin.com/posts/isayahc_embodiedai-agentobservability-robotics-activity-7516125244617842689-EP8A
- SSI company updates: https://www.linkedin.com/company/strategic-systems-international/

The SSI link is a company feed, not an individual announcement permalink; replace it when a stable post URL is available. The quotation is 19 words. Current project descriptions distinguish alpha/prototype capabilities, synthetic data, and physical deployment boundaries.

## Editing

- `index.html`: copy, project links, recognition, and contact
- `styles.css`: responsive layout and visual design
- `assets/mark.svg`: geometric site mark
- `.nojekyll`: serves the static files without Jekyll processing
- `landing-page/index.html`: compatibility redirect for the former project URL

No generated build artifacts or secrets are needed.
