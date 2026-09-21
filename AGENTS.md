# Repository Guidelines

## Project Structure & Module Organization

This repository is a Belarusian-language critical-thinking workbook built from Markdown files. `README.md` is the course entry point and module index. Lesson notes live in `notes/`, named by sequence and topic, for example `notes/02-3-choosing-useful-model-under-uncertainty.md`. Keep shared terminology in `GLOSSARY.md`, source context in `SOURCES.md`, and contributor-facing policy in `CONTRIBUTING.md`. Obsidian workspace settings under `.obsidian/` are not course content.

When adding a module, update the README contents and tool-selection table, previous/next navigation, and any relevant glossary or source notes.
For an existing numbered draft, follow the repository skill at `.agents/skills/add-course-module/SKILL.md` to integrate it across the course.

## Development and Validation Commands

There is no build step, package manager, or application runtime. Review Markdown directly or through GitHub/Obsidian preview.

- `rg --files -g '*.md'` lists all course documents.
- `rg -n "term" . -g '*.md'` checks terminology and cross-document references.
- `git diff --check` detects whitespace errors before committing.
- `git diff -- '*.md'` reviews only documentation changes.

Also open every changed relative link. After renaming a file, search for its old path across the repository.

## Writing Style & Naming Conventions

Write course content in Belarusian, primarily classical orthography, and preserve established terminology. Use English method names at first mention when they improve searchability. Keep prose direct and instructional; distinguish facts, educational adaptations, and proposals. Define unfamiliar terms and add primary sources for new empirical claims.

Use ATX headings (`#`, `##`), standard Markdown tables, and relative links. Name lesson files as `NN-N-descriptive-topic.md`: use the module number followed by a lowercase English kebab-case summary, rather than a number alone. A lesson should generally follow: review, purpose, core distinctions, example, pitfalls, practice, collapsible self-check, and mastery criterion. Keep one lesson usable in roughly 25–30 minutes.

## Testing Guidelines

No automated test suite exists. Validation consists of checking local links, rendering changed Markdown, confirming table and `<details>` formatting, and reviewing terminology against `GLOSSARY.md`. Ensure navigation forms an unbroken sequence from `README.md` through the last lesson.

## Commit & Pull Request Guidelines

History currently uses short, imperative summaries such as `Initialize`; follow that concise style and keep each commit focused on one purpose. Pull requests should explain what changed and why, list affected modules, link relevant issues or sources, and mention link/rendering checks performed. Include screenshots only when a rendering problem is easier to assess visually.

Never include private correspondence, identifiable personal details, or substantial copied passages without appropriate rights.
