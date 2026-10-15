# AGENTS.md

## Project type

Static HTML/CSS course practice site (高级网页设计). No build step, no dependencies, no CDN, no package manager. Open files directly in a browser.

## Entry point

`index.html` is the hub page — it links to every practice page in the directory. Start here.

## Structure

- Numbered practice pages (`2-1.html` … `10-3.html`) each cover one topic (layout, flexbox, CSS3 selectors, animation, responsive design).
- Most pages use inline `<style>` blocks. `store.html` is the only page with external CSS (`css/style.css`).
- `images/` holds assets referenced by `store.html`. `图片/` contains additional images.
- Some filenames contain Chinese characters — `index.html` hrefs are percent-encoded (e.g. `5-1%E5%B1%82%E5%8F%A0%E4%B8%8E%E7%BB%A7%E6%89%BF.html`). Preserve this encoding when adding links.

## Naming convention

All CSS class names, ID names, and JS variables must start with `zhou` (e.g. `zhou-page`, `zhou-unit-card`).

## Prompt log

Before executing any prompt, append it to `zhou_prompt.md` in the repo root (never overwrite). Entry format: timestamp, model, prompt text.

## Index rule

Every new HTML page must be added to the page grid in `index.html` before completing the task. Use the next sequential "Practice NN" label and percent-encode any non-ASCII filenames in the href.

## Verification

No lint, typecheck, or test commands exist. Verify changes visually in a browser. There is no codegen, migrations, or generated code.
