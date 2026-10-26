# AGENTS.md

## Project type

Static HTML/CSS course practice site (高级网页设计). Native (vanilla) HTML/CSS/JavaScript only — no third-party libraries or frameworks, no remote CDN. No build step, no dependencies, no package manager. Open files directly in a browser.

## Icon rule

Icons must use the iconfont set from the `font` directory (iconfont.css / iconfont.js / iconfont.ttf / iconfont.woff / iconfont.woff2). The in-repo copy lives at `cdn/iconfont/` — reference it from there so pages stay self-contained. Do not introduce icon libraries (FontAwesome, Lucide, etc.) or fetch them from a CDN.

Legacy exception: pages 13-1–13-4 were built earlier with local FontAwesome/Lucide copies under `cdn/`; leave them unchanged unless asked to refactor.

## Data fetching rule

When a page needs server-side data, obtain it with the native `fetch` API (part of the browser, consistent with the no-library rule). Local static JSON files may be fetched directly; there is no backend in this project.

## Entry point

`index.html` is the hub page — it links to every practice page in the directory. Start here.

## Structure

- Numbered practice pages (`2-1.html` … `10-3.html`) each cover one topic (layout, flexbox, CSS3 selectors, animation, responsive design).
- Most pages use inline `<style>` blocks. `store.html` is the only page with external CSS (`css/style.css`).
- `images/` holds assets referenced by `store.html`. `图片/` contains additional images.
- Some filenames contain Chinese characters — `index.html` hrefs are percent-encoded (e.g. `5-1%E5%B1%82%E5%8F%A0%E4%B8%8E%E7%BB%A7%E6%89%BF.html`). Preserve this encoding when adding links.

## Naming convention

All variable names, CSS class names, and ID names must start with `zxzy_` (e.g. `zxzy_page`, `zxzy_unit_card`). Legacy pages may still use the older `zhou-` prefix — do not mass-rename unless asked.

## Page comment rule

Every NEW HTML file must include a header comment immediately after `<!DOCTYPE html>`, containing the author name, creation time, the AI model used to build it, and a short description of the page's feature:

```html
<!-- 姓名：周徐倬玚，建立时间：YYYY-MM-DD HH:mm，大模型：<模型名，如 GLM-5.3-Flash>，功能名称：<页面功能简述> -->
```

Existing pages keep their current comments; do not retroactively edit them unless asked.

## Prompt log

Before executing any prompt, append it to `zhou_prompt.md` in the repo root (never overwrite). Entry format: timestamp, model, prompt text.

## Index rule

Every new HTML page must be added to the page grid in `index.html` before completing the task. Use the next sequential "Practice NN" label and percent-encode any non-ASCII filenames in the href.

## Verification

No lint, typecheck, or test commands exist. Verify changes visually in a browser. There is no codegen, migrations, or generated code.
