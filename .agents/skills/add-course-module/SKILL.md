---
name: add-course-module
description: Integrate an existing lesson draft into this thinking-toolkit Markdown course, including its filename, reading sequence, README, glossary, and source notes. Use when a user adds a numbered module such as notes/03-1.md and asks to add it to the whole course.
---

# Add a course module from existing text

Treat the supplied draft as the source of the lesson. Preserve its argument and examples while editing for the repository's Belarusian terminology, primarily classical orthography, and readable Markdown. Do not invent research findings, citations, or substantive claims to fill a template. Read `AGENTS.md` and `CONTRIBUTING.md` before changing course material.

1. Inspect the worktree and read the draft, adjacent lessons, `README.md`, `GLOSSARY.md`, and `SOURCES.md`. Identify the intended module number and position from the draft and existing sequence. Preserve unrelated user edits. If the position or lesson identity is genuinely ambiguous, ask before renumbering existing modules.
2. Give a generic draft filename such as `notes/03-1.md` a descriptive lowercase English kebab-case suffix, following `notes/02-3-choosing-useful-model-under-uncertainty.md`. Keep the visible heading in Belarusian with the dotted module number, such as `03.1`. Move the draft without losing its content; check for references to its old path.
3. Adapt the draft into a usable standalone lesson. Include links to the README and neighboring lessons, a brief connection to prior material, clear purpose, examples, a practice prompt, a collapsible `<details>` self-check, and a mastery criterion when the source supports them. Keep additions proportionate to a roughly 25–30 minute lesson. If essential content is absent, surface the gap rather than presenting invented material as the author's text.
4. Add the lesson in numeric order to the README contents and tool-choice table. Link the preceding lesson forward and the new lesson back; if another lesson follows, connect both directions. The last lesson has no forward link. Update the glossary for genuinely new or changed terms. Update `SOURCES.md` for source provenance, editorial caveats, module counts, and range statements that actually change. Do not resurrect the removed final practice. Change `AGENTS.md` or `CONTRIBUTING.md` only if their general contributor guidance becomes inaccurate.
5. Search all Markdown for the old filename, stale last-module/count statements, and dead references. Check every local Markdown link, navigation order, `<details>` balance, and `git diff --check`. Review the diff for unintended rewrites, then report what was integrated and any source or verification limits. Commit or push only when separately requested.
