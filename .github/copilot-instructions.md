This repository is a small static HTML/CSS resume site. Keep instructions short, specific, and focused on making small, non-destructive edits suitable for GitHub Pages deployment.

Key facts (big picture)
- Single-page static site: `index.html` is the canonical content. `style.css` holds presentation. `Jason_Saari_Oct_2025_PDF.pdf` is an attached printable resume.
- CI/CD: `.github/workflows/static.yml` uploads the repository to GitHub Pages on pushes to `main`. Any change to HTML/CSS will be deployed automatically.

What to change and what to avoid
- Safe edits: content updates in `index.html` (typos, dates, contact links), CSS tweaks in `style.css`, and README improvements. These are low-risk and deploy immediately.
- Avoid: changing workflow files, repository settings, or renaming `index.html` unless the change includes an updated workflow. Don't remove the PDF file unless asked.

Conventions & patterns in this repo
- Content-first, single HTML page: structure is semantic (header, section, job blocks). Follow existing classes (`.summary`, `.skills`, `.work-history`, `.job`) when adding content.
- Styling: `style.css` uses simple global selectors and responsive @media rules. Prefer adding new classes for non-trivial layout changes rather than editing many global rules.
- Links: use absolute URLs for external sites and relative paths for local assets (e.g., `style.css`, `Jason_Saari_Oct_2025_PDF.pdf`).

Examples (concrete edits)
- To add a new skill, add an `<li>` under the `.skills` <ul> in `index.html`.
- To correct phone number formatting, update the `<a href="tel:+12692676650">` anchor in `index.html`.
- To change the header color, edit `header h1` color in `style.css` (currently `#35503D`).

Developer workflows & checks
- Deployment: pushing to `main` triggers `.github/workflows/static.yml` to publish to GitHub Pages. No local build step required.
- Quick local preview: open `index.html` in a browser. For iterative CSS/HTML changes, live-server or VS Code Live Preview can be used but are optional.

Searchable anchors to reference in suggestions
- `index.html` — primary content
- `style.css` — styling and responsive rules
- `.github/workflows/static.yml` — deployment pipeline
- `README.md` — repo description

Behavior for AI coding agents
- Keep PRs tiny and focused (single content or style change). Use clear commit messages like "Fix typo in Summary" or "Add Terraform to skills list".
- When changing HTML structure, ensure the visual layout remains intact on desktop and mobile (check existing @media rules).
- Include a brief summary in PR descriptions describing why the change is needed and which files changed.

If you need more context or larger feature work
- Ask for guidance before renaming or adding new pages (e.g., adding a blog or multi-page site). That will require workflow updates and a review of GitHub Pages settings.

Contact/owner
- This repository represents Jason Saari's resume. For any content decisions beyond spelling/formatting, request clarification from the owner.

If anything here looks incomplete, tell me what to clarify and I'll iterate.
