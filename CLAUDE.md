# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Fishy is a marketing/landing website for an iOS fishing journal app. The website is a static site with no build system.

## Structure

- `index.html` - Landing page with app description and features
- `privacy.html` - Privacy policy page
- `support.html` - Support page with FAQs

## Development

To preview, open any HTML file directly in a browser or use a local server:
```bash
python3 -m http.server 8000
```

## Patterns

- **Bilingual content**: All pages support English (EN) and Finnish (FI) via a language toggle. Content is duplicated with `lang-en` and `lang-fi` CSS classes, controlled by adding `en` or `fi` class to `<body>`.
- **Styling**: CSS is inline in each HTML file (no external stylesheets). Each page has its own complete styles.
- **JavaScript**: Inline at bottom of each page. The `setLanguage()` function handles language switching and persists preference to localStorage under `fishy-lang` key.
