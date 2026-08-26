# shalini-karthyk.github.io

Personal portfolio site for Shalini Karthyk. Static HTML, no build step, served by GitHub Pages from the repository root.

---

## Why this site exists

This is a job-search asset, not a design exercise. Its single job is to help Shalini get hired as a mid-level computational biologist. Judge every content and design decision against that.

**Target roles:** Computational Biologist · Bioinformatics Scientist · Genomics Scientist. Mid-level (Scientist / Scientist II), roughly the $120–170K band.

**Target employers:** Big pharma first — AbbVie, Lilly, Novartis, AstraZeneca, Moderna and peers. Well-capitalized late-stage biotech second. Not early-stage startups. Not academia.

**Geography:** Boston / Cambridge, MA. Hybrid, remote, or onsite all acceptable.

**Domain she wants:** Human disease biology — target identification, multi-omic analysis, machine learning on biological data. She is deliberately steering away from the microbial and environmental work that dominates her current job.

**Her own framing, in her words:** she wants to be the bridge between biology and computer science, and point it at disease. Not a pipeline operator. Not a data engineer. A scientist who can take a biological question and build whatever it takes to answer it.

---

## The two problems this site has to solve

**1. She has an MS, not a PhD.** Roughly half of the postings she's targeting hard-gate on the doctorate. The site can't fix that. It can make it matter less — by showing publications, real ownership, shipped infrastructure, and depth that reads as post-doctoral in substance if not in title.

**2. Her current job reads as environmental microbiology.** Her most recent and most prominent role is enzymes and microbes. Everything human — NK cells, CD8+ T cells, erythroid differentiation, kidney organoids, DMD — sits in older roles. All three publications are human immunology. A recruiter who reads the top third and stops will misfile her.

Mitigations currently in place: Publications sit *above* Work. The Breaking candidate-discovery project is written in target-ID vocabulary, not enzyme-screening vocabulary. The hero statement plants human immunology before the reader reaches Breaking. Preserve these unless replacing them with something better.

---

## Content rules — do not break these

- **No fabrication.** Never invent a metric, tool, collaborator, date, title, or outcome. If a claim isn't already in the content, ask before adding it.
- **No percentages.** Counts and absolute scale only. This is a deliberate standing rule from her resume work.
- **No visa or work-authorization language anywhere on the page.** That belongs only in application forms. She needs an H-1B transfer; the site must never mention it.
- **No photo** unless she explicitly asks.
- **No scientific figures or plots.** She has declined to publish them.
- **Employer-sensitive detail.** The Breaking specifics — 6,000+ sequences, 863 proteins, 5,800-gene genome, 54 virulence hits, 53 mobile genetic elements, 6 nominated candidates — are *not* confirmed as cleared for public publication. Do not add new ones. Flag before amplifying existing ones.
- **Publication status is exact.** One 2026 bioRxiv preprint, two under review. Never upgrade "under review" to "published."
- **Concurrency stays visible.** The Institute for Experiential AI role overlaps Breaking from Nov 2024. Both employers knew. The page says so explicitly, because unexplained overlap triggers background-check friction. Don't quietly remove that flag.

---

## Design system

**Palette**

| Token | Hex | Use |
|---|---|---|
| `--bg` | `#EBECE6` | page ground |
| `--surface` | `#F6F7F2` | project cards, chips |
| `--ink` | `#13171A` | primary text |
| `--ink-2` | `#4B5257` | body prose |
| `--ink-3` | `#6C7278` | captions, labels |
| `--rule` | `#C8CAC3` | borders |
| `--rule-soft` | `#D9DBD4` | internal dividers |
| `--deep` | `#1B3A5F` | structure, project titles, links |
| `--signal` | `#9E2B62` | accent — sparing, high-value only |

**Type**

- **Archivo** (variable, `wdth` 100–125) — headings, org names, section titles. The grotesque is "the built side."
- **Newsreader** — body prose and the hero's italic half-line ("Biology asks."). The serif is "the biology side."
- **IBM Plex Mono** — dates, labels, tool chips, capability lists.

**The two signature devices. Preserve these.**

1. **The hero headline is set in two typefaces.** *"Biology asks."* in serif italic, deep blue. *"I build what answers it."* in expanded Archivo, ink black. The typographic split **is** the positioning: biology on one side, engineering on the other, her as the bridge. Don't flatten it to one face.

2. **Every project opens with a short title naming what it answered**, set in Archivo (not serif italic — that convention was retired 2026-08). This still has to stop the page reading as a tool inventory: the title should name the biological problem or system, not the tool stack. Any project added later must have a title in that spirit.

**Restraint.** One accent color, used rarely. Motion limited to scroll reveals and hover states. No gradients, no stock icons, no generic hero graphic, no numbered `01 / 02 / 03` markers. `prefers-reduced-motion` is respected and must stay that way.

---

## Structure

```
Nav → Hero → Publications → Work → Capabilities → Education + Academic projects → Contact
```

**Work** is reverse chronological by her explicit request: Breaking → Institute for Experiential AI → Fulcrum Therapeutics → Brigham and Women's Hospital → Harvard Medical School. Projects are nested inside the role they happened in.

Work and Experience are **one merged spine**. An earlier version split them and the two sections said the same things twice. Do not split them back apart.

---

## Quality floor

- Responsive down to 360px
- Visible keyboard focus on every interactive element
- Semantic landmarks, exactly one `h1`
- Contrast: body text ≥ 4.5:1, large text ≥ 3:1
- No build step, no framework, no external JS dependencies
- Page renders and reads correctly with JavaScript disabled
- Google Fonts is the only external request

---

## Git rules

- **Never push. Never force-push. Never merge into the default branch** unless Shalini says so explicitly in that session. "Looks good" is not authorization to push.
- Work on the redesign branch. Commit freely, in small increments, with descriptive messages.
- **Preserve these files if they exist**, at every step: `CNAME`, `.nojekyll`, `LICENSE`, any `google*.html` or similar site-verification files, and `.github/`. These are what silently break a Pages site when deleted.
- The old site is recoverable from git history and from the `pre-redesign` tag. Deleting it from the working tree is safe.
