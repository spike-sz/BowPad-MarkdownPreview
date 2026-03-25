# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/), and this project adheres to [Semantic Versioning](https://semver.org/).

## [1.10] - 2026-03-25

### Added

- **TOC sidebar navigation** — Auto-generated table of contents sidebar on the left side of the preview page
  - Extracts all headings (h1–h6) with proper hierarchy indentation
  - Scroll tracking: automatically highlights the current section in the TOC as you scroll
  - Smooth scroll: clicking a TOC item scrolls smoothly to the target heading
  - Collapsible toggle button to show/hide the sidebar
  - TOC auto-scrolls to keep the active item visible
  - Supports duplicate heading text (appends `-1`, `-2`, etc. to IDs)
  - CJK-friendly heading ID generation

### Fixed

- **Anchor link navigation** — Fixed in-page anchor jumps failing due to the `<base>` tag overriding fragment URLs; TOC links now use `data-target` attribute with `scrollIntoView()` instead of `#` hash links
- **Relative image path resolution** — Moved image path resolution from HTML `<base>` tag to parser-level `basePath` prefix, avoiding the `<base>` tag side effect on anchor links
- Fixed invalid CDN directory links in README (replaced with official project URLs for highlight.js and MathJax)

## [1.0] - 2026-03-15

### Added

- Initial release of MarkdownPreview plugin for BowPad
- Full Markdown rendering with Typora-like styling
  - ATX and Setext headings
  - **Bold**, *italic*, ~~strikethrough~~, ==highlight==, ^superscript^, ~subscript~
  - Fenced and indented code blocks with syntax highlighting (highlight.js)
  - Tables with column alignment
  - Ordered and unordered lists
  - Task lists (checkboxes)
  - Nested blockquotes
  - Images and links (inline and reference-style)
  - Horizontal rules
  - Math blocks via MathJax (`$$...$$`)
- Dark mode support — automatically adapts to system color scheme
- Per-file HTML output with path-based hashing to avoid name collisions
- Relative image path resolution from the source Markdown file
- Two preview modes:
  - **Click** — Render to HTML and open in default browser
  - **Shift+Click** — Output HTML to a new BowPad tab
- HTML output written via `ADODB.Stream` with UTF-8 encoding
