# Assignment creation notes (QRI-2026)

Notes for creating and editing assignments in this repo. Use this file when building the next assignment (e.g. Assignment 06) so the process is consistent.

## Repository boundaries

- **Edit only:** `QRI-2026` repository. Do not modify the parent `QR-A` repository.
- **Do not change:** Existing assignment files or existing exercise files. Only add new ones.
- **Read-only use of QR-A:** You may read chapter `.qmd` files, `Exer-*.qmd`, and `Drill-*.qmd` in QR-A for content and structure; do not edit them.

## Assignment file pattern (from Assignment-04)

- **Location:** Root of QRI-2026, e.g. `Assignment-05-CH8.qmd`.
- **YAML:** `title`, `subtitle` (e.g. "Chapter 8 of the QR-A book").
- **Includes (in order):** `_use_webr.qmd`, then R chunk with `library(devoirs)`, `library(mosaicCalc)`, `source("_start-up.R")`, then `_devoirs.qmd`.
- **Drill callout:** Collapsible note linking to `https://dtkaplan.github.io/QR-A/Drill-XX-<topic>.html`. Only add if a Drill for that chapter exists in QR-A.
- **Chapter block:** Collapsible callout "Chapter N", inside it `id <- "aN-chX"`, then `{.panel-tabset}` with tabs "1.", "2.", ... each `{{< include _exercises/<name>.qmd >}}`.

## Exercise file pattern

- **Location:** `QRI-2026/_exercises/`. Naming: `adjective-noun-verb.qmd` (e.g. `bear-climb-mountain.qmd`).
- **YAML:** `id` (kebab-case same as filename), `created`, `attribution`, `use` (e.g. "Chapter 8 exercise").
- **R setup:** Optional `include=FALSE` chunk with `library(devoirs)`, `library(mosaicCalc)` for stand-alone testing. If exercises use storybook functions, include webr chunk with `{{< include _software/storybook-functions.r >}}`.
- **Structure:** Wrapper `::: {#exr-<id>}` ... `:::`. Comment at end `<!-- end of exr-<id> -->`.
- **Answer marking:**
  - **MCQ:** Use `{mcq}` block; mark correct option with `[correct]` (and optional `[correct hint: ...]`).
  - **Multiple choice / short answer:** `devoirs_set(choices = c(...), correct = <value>, id = "unique-id")`.
  - **Free response:** `devoirs_text("unique-id", rows = n)`.
- **Balance:** Majority MCQ, some free response. Exercises can be medium length (several MCQs + 1–2 free response per exercise).

## Assignment 05 (Chapter 8) – Composing functions

- **Source chapter:** `QR-A/Chap-08-composing-functions.qmd`.
- **Drill:** `Drill-08-composing-functions.qmd` exists in QR-A → link in assignment.
- **Exercises:** 5, medium length, mix of MCQ (majority) and free response.
- **Quarto:** Do not update `_quarto.yml`; instructor updates after exercises are finalized.

### Ch 8 topics to cover

- Linear combinations: \(h(x) = a\,f(x) + b\,g(x)\); coefficients; specifying ingredient functions.
- Two inputs: \(h(x,z) = a\,f(x) + b\,g(z)\); steady/flat; when to use magnitude() or hillside() instead of steady().
- Function multiplication: \(h(x)=f(x)g(x)\) (one input) vs \(j(x,z)=f(x)g(z)\) (two inputs); interaction term steady(x)×steady(z).
- Pipelining: \(f(g(x))\) vs \(g(f(x))\); interior vs exterior; single argument only; input transformation \(g(x)=ax+b\).
- Polynomials: linear combinations of monomials (flat, steady, steady×steady, …); quadratic \(ax^2+bx+c\).

### Assignment 05 exercise files (created)

| # | Filename | Focus |
|---|----------|--------|
| 1 | falcon-catch-wind.qmd | Linear combinations, coefficients, ingredient functions |
| 2 | otter-build-dam.qmd | Multiplication vs pipelining |
| 3 | moth-seek-flame.qmd | Two-input functions / interaction |
| 4 | crow-open-walnut.qmd | Polynomials, quadratics, monomials |
| 5 | newt-cross-log.qmd | Input transformation, pipelining |

---

## For next time (Assignment 06)

- Decide which chapter(s) from QR-A to use and read the corresponding `Chap-*.qmd` and optionally `Exer-*.qmd`.
- Check if a Drill exists in QR-A for that chapter; if yes, add the drill callout with link to `https://dtkaplan.github.io/QR-A/Drill-XX-<topic>.html`.
- Create `Assignment-06-CHX.qmd` (or `Assignment-06-CHX-CHY.qmd` if two chapters) following the same structure as Assignment-05.
- Create 3–5 new exercise files in `_exercises/` with new adjective-noun-verb triplets; do not reuse triplets from this list or from existing exercises (bear, calf, daisy, deer, falcon, fox, moth, newt, otter, owl, puppy, rabbit, spider, squirrel, titmouse, wolf, crow).
- Mark correct answers: `[correct]` in `{mcq}`, `correct = ...` in `devoirs_set`, and use `devoirs_text` for free response.
- Do not update `_quarto.yml`; instructor will do that when the assignment is finalized.

---

*Last updated during Assignment-05 creation (Feb 2026).*
