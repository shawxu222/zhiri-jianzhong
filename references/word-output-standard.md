# Word Output Standard

Use this reference when the user asks this skill to output a Word `.docx`, match a WeChat draft format, preserve an editorial template, or handle source images/tables.

This public version does not include a private `.docx` template asset. If a user provides a local template, infer only reusable structure and visual rhythm from it. Do not copy old article text into new outputs.

## Fixed Article Blocks

Every Word deliverable should use this order:

1. title
2. `引言：`
3. introduction paragraphs
4. body sections with Chinese numerals, such as `一、……`, `二、……`
5. `结语：`
6. conclusion paragraphs
7. `【原文作者】`
8. source/author note
9. `原文链接：` plus URL if provided
10. optional editorial credit block, if the user provides one

Use an editorial credit block only when the user provides names or roles. If no credit block is provided, omit it or use neutral placeholders in drafts that are clearly marked as placeholders.

```text
【编辑委员会】
指导：……
翻译：……
校核：……
编务：……
设计：……
```

Do not invent personal names, affiliations, private committee roles, or recurring staff information.

## Section Intent

### Title

Use the final recommended title. Prefer a concise policy/strategy angle over a marketing headline.

### 引言

Use `引言：` as the heading. The introduction should:

- state why the Japanese source is worth reading
- establish the China-facing lens
- summarize the core thesis in 1-3 short paragraphs
- mention the Japanese source and author only when it helps orient the reader

### 正文

Use numbered sections with Chinese numerals. Each section should be MECE and argument-bearing, not a generic topic label.

Prefer section headings like:

- `一、……`
- `二、……`
- `三、……`

Within each section, use paragraph-level "总-分": first sentence gives the point, following sentences explain mechanism, example, evidence, or implication.

### 结语

Use `结语：` as the heading. The conclusion should return to the opening lens, name the most important mechanism or boundary, and close with a restrained think-tank style reflection.

### 原文作者

Use `【原文作者】` as the heading. Include:

- source outlet/publication
- author name and role if provided
- original title if useful
- one sentence explaining that the text was compiled by the editorial team for Chinese readers

Example pattern:

```text
摘自《……》，作者为……。原文经编辑团队编译，方便中文读者更好地理解。

原文链接：
https://...
```

## DOCX Production Requirements

When creating a Word file:

- Use the document-generation workflow from the documents skill.
- Prefer preserving the house draft's simple paragraph style over inventing a new visual design.
- Keep headings and body paragraphs clean and editable; do not turn text into images.
- Use real Word tables for tables.
- Use inline images where possible, with captions immediately below.
- Render the final DOCX to page images and inspect every page when the environment supports it. If rendering fails because LibreOffice or native dependencies are unavailable, still deliver the DOCX but state that visual render QA could not be completed.

## Tables From Source Articles

If the original Japanese article contains an actual table, rebuild it as a native Word table:

- translate all cells into Simplified Chinese
- preserve numbers, units, dates, rankings, and footnotes
- keep the table editable
- add a short Chinese caption or lead-in explaining why the table matters
- avoid dense tables when the same information reads better as prose or bullets

If the source table is embedded as an image, prefer recreating it as an editable Word table when the contents are legible. Note OCR uncertainty in editor notes.

## Images And Figure Text

Handle images according to image type:

- Photo or illustration with no important embedded text: preserve the image and translate the caption/alt text.
- Chart, screenshot, or diagram with Japanese text: extract the text, translate it, and choose the safest localization method.
- Table-like image: recreate as a native Word table when possible.
- Diagram or chart with labels: either recreate as an editable Word-friendly figure or overlay Simplified Chinese labels on a copy of the image.

Directly replacing Japanese text inside a raster image is possible only when the text is legible and the layout is simple enough. Treat it as a high-QA task:

- preserve the original image separately when useful
- avoid hiding uncertain OCR results
- visually inspect the edited image and final DOCX
- mention unresolved OCR or layout uncertainty in editor notes

Default preference: make translated visual information editable in Word rather than baked into pixels, unless the user specifically asks for localized images.

## Delivery

When the Word file is ready, return the `.docx` path/link and a short note about:

- whether visual render QA passed or was unavailable
- any image/table OCR uncertainty
- any source fields missing from the original article, such as author, date, or URL
