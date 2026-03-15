# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/), and this project adheres to [Semantic Versioning](https://semver.org/).

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
