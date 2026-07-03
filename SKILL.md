---
name: edit-japan-tech-policy-wechat
description: Transform Japanese technology, science policy, innovation, and soft-science articles, especially pasted Japanese news or magazine source articles, into polished Simplified Chinese WeChat public-account drafts and optional Word `.docx` deliverables for China-facing tech policy researchers, policymakers, and think-tank readers. Use when Codex needs to translate, compile, restructure, edit, localize, headline, quality-check, or package Japanese-source content into rigorous, readable Chinese articles with a clear storyline, Pyramid Principle structure, MECE sections, Japanese-perspective context, restrained policy-analysis style, and a configurable WeChat draft Word format.
---

# Edit Japan Tech Policy Wechat

## Core Mandate

Produce a high-standard Chinese compilation article, not a literal sentence-by-sentence translation. Preserve the source article's facts and Japanese perspective while rebuilding the narrative for Chinese readers who care about technology policy, innovation systems, industrial strategy, and soft-science research.

Prioritize four values in this order:

1. Source fidelity
2. Reader relevance for China-based policy and research audiences
3. Clear argument structure
4. Smooth WeChat readability

## Required References

For any substantive article translation, compilation, restructuring, or style review, read `references/editorial-standard.md` before drafting. Use it for audience assumptions, article structure, translation rules, style constraints, and the final quality checklist.

For publishable WeChat drafts, house-style matching, or any request that mentions successful prior articles, also read `references/success-sample-patterns.md`. Use it to reproduce the approved article architecture: "overall thesis first, MECE parts second, paragraph-level topic sentence before supporting detail".

For Word `.docx` output, template matching, image/table localization, or any request that asks for a file deliverable, also read `references/word-output-standard.md`.

## Default Workflow

1. Identify the source premise: title, outlet, publication date if provided, article type, main claim, key facts, quoted actors, and the Japanese context the original assumes.
2. Define the China-facing editorial angle: explain why this Japanese case, policy move, company decision, research result, or social debate matters to Chinese technology-policy readers.
3. Build a one-sentence thesis before drafting. Put the conclusion or highest-value insight near the beginning rather than saving it for the end.
4. Reorganize the source into MECE sections. Each section should answer a distinct reader question such as "what happened", "why Japan cares", "what mechanism is at work", "what is new", and "what China-facing readers can learn".
5. Translate meaning, not syntax. Convert Japanese long sentences, implicit subjects, and publication-specific assumptions into precise Simplified Chinese prose.
6. Add context only when it is necessary for comprehension. Clearly separate source-based facts from editor inference or external background. Verify current or unstable facts before adding them.
7. Produce a publishable draft first, then add concise editor notes about uncertain terms, missing dates, assumptions, or points that may need source verification.

## Default Output

Unless the user asks for a different format, return:

- `标题候选`: 3 restrained WeChat-ready titles
- `推荐标题`: the strongest title with the clearest policy angle
- `导语`: 1-2 short paragraphs that state the article's core value
- `正文`: a polished Simplified Chinese article with meaningful section headings
- `编辑备注`: brief notes on source fidelity, uncertain translations, missing context, or optional follow-up checks

If the user asks for Word output, create a `.docx` draft instead of only returning text. Follow the configurable article blocks in `references/word-output-standard.md`: title, `引言：`, body sections, `结语：`, `【原文作者】`, original link if available, and optional editorial credits if provided.

If the user asks only for a translation, still improve Chinese readability while preserving the original order more closely. If the user asks for a publishable article, restructure more aggressively.

## Source Discipline

Do not invent facts, numbers, dates, quotes, institutional relationships, or policy background. If the source does not support a claim, either omit it, mark it as an editorial inference, or ask the user for permission to verify externally.

When working from copyrighted news content, create a transformative compilation: summarize, restructure, explain, and analyze. Avoid reproducing the original article's paragraph order and distinctive expression as a full-length close translation unless the user explicitly confirms they have rights and the task permits it.

## Voice

Write in professional Simplified Chinese: analytical, calm, concrete, and readable. Avoid hype-driven WeChat clichés, exaggerated certainty, empty praise, and generic AI transitions. The result should sound like a careful think-tank editor with strong Japanese context, not a marketing account.
