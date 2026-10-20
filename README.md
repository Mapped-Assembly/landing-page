# Mapped Assembly landing page

A buildless, responsive website for Mapped Assembly. Plain HTML and CSS; no JavaScript, dependencies, analytics, or external fonts.

## Preview locally

From the repository root:

```bash
python3 -m http.server 8000
```

Open http://localhost:8000. Stop with Ctrl+C.

## Publish on GitHub Pages

After merging the website PR, open **Settings → Pages** and select **Deploy from a branch**, **main**, **/ (root)**, then Save. No build workflow is needed. Relative asset paths work at the project URL:

https://mapped-assembly.github.io/landing-page/

This repository was private when the page was prepared. GitHub Pages for a private organization repository requires a supported paid organization plan; otherwise the owner must choose to make the repository public. This PR does not change visibility or enable publishing.

For the root address https://mapped-assembly.github.io/, use a repository named Mapped-Assembly.github.io. Renaming this repository or configuring a custom domain is a separate owner decision.

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

No generated build artifacts or secrets are needed.
