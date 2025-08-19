---

marp: true
math: katex
paginate: true
footer: 'Page \$current / \$total — [24f2003053@ds.study.iitm.ac.in](mailto:24f2003053@ds.study.iitm.ac.in)'
theme: custom
-------------

<style>
:root { --accent: #0ea5e9; --muted: #6b7280; }
/* Custom Marp theme */
@theme custom {
  section { font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, "Helvetica Neue", Arial, sans-serif; }
  h1, h2, h3 { color: var(--accent); letter-spacing: .3px; }
  code, pre { font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", monospace; }
  section.lead { justify-content:center; align-items:center; text-align:center; }
  section.invert { background:#0b1220; color:#eef2ff; }
  .pill { padding:.2em .65em; border-radius:9999px; background:var(--accent); color:white; font-weight:600; }
  .muted { color: var(--muted); }
}

/* Extra slide polish */
section { padding: 64px; }
img[alt~="bg"] { opacity: .18; }
</style>

<!-- _class: lead -->

# **Product Documentation**

### Maintainable with Marp + Git

**Author:** Krish Rohilla
**Email:** [24f2003053@ds.study.iitm.ac.in](mailto:24f2003053@ds.study.iitm.ac.in)

<span class="pill">Marp</span> <span class="muted">Markdown → HTML/PDF/PPTX</span>

---

## Why Marp for Docs Presentations?

* Single source: **Markdown** in Git for easy reviews & diffs
* Export to **HTML, PDF, PPTX** with marp-cli
* Custom theming via CSS (**this deck uses a custom theme**)
* Page numbers via `paginate: true` & `footer`
* KaTeX math for algorithms and formulas

---

<!-- _class: invert -->

<!-- _backgroundImage: url('https://images.unsplash.com/photo-1515879218367-8466d910aaa4?q=80&w=1600&auto=format&fit=crop') -->

<!-- _backgroundSize: cover -->

<!-- _backgroundPosition: center -->

# Background Image Slide

Use slide directives for backgrounds without leaving Markdown.

**Contact:** [24f2003053@ds.study.iitm.ac.in](mailto:24f2003053@ds.study.iitm.ac.in)

---

## Custom Styling via Directives

* Slide classes: `<!-- _class: invert -->` (see previous slide)
* Backgrounds: `<!-- _backgroundImage: url('...') -->`
* Per‑slide footer: `<!-- _footer: 'Page $current — Docs' -->`
* Accent UI: <span class="pill">pill badge</span> using custom theme CSS

---

## Math: Algorithmic Complexity

We can derive the closed form for a simple nested loop:

$T(n) = \sum_{i=1}^{n} i = \frac{n(n+1)}{2} = O(n^2)$

And for a divide-and-conquer recurrence with the Master Theorem:

$T(n) = 2\,T\!\left(\frac{n}{2}\right) + n \;\Rightarrow\; T(n) = O(n\log n)$

---

## Code Snippet (fenced code block)

```python
from dataclasses import dataclass

@dataclass
class Feature:
    name: str
    done: bool = False

features = [Feature("Export to HTML", True), Feature("Export to PDF"), Feature("Theme CSS", True)]
print("Planned:", ", ".join(f.name for f in features if not f.done))
```

Notes:

* Works across HTML/PDF/PPTX exports
* Syntax highlighting depends on the chosen renderer/theme

---

## Build & Export (CLI)

```bash
# Install CLI (Node.js required)
npm install -g @marp-team/marp-cli

# Live preview
marp -s .

# Export formats
marp slides.md --html --allow-local-files           # HTML
marp slides.md --pdf --allow-local-files             # PDF
marp slides.md --pptx --allow-local-files            # PowerPoint
```

The Markdown source (`slides.md`) stays the single source of truth in Git.

---

## Repository Layout

```
📦 product-docs-preso
├─ slides.md            # ← This Marp deck (single source)
├─ README.md            # How to build/export
└─ assets/
   └─ bg.jpg            # Optional local background(s)
```

*Pro tip:* Use `?v=1`, `?v=2`, etc., when viewing the raw file on GitHub Pages/Raw to bust caches.

---

## Contact

For questions, reach out at **[24f2003053@ds.study.iitm.ac.in](mailto:24f2003053@ds.study.iitm.ac.in)**

Thank you!
