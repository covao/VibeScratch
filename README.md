# VibeScratch

![Demo Image](./demo.gif)

## Overview

VibeScratch is a single-file web app for building and editing Markdown content as draggable blocks. It features a two-panel layout: a **PALETTE** on the left for source blocks, and a **Block Editor** on the right for composing your document.

## Quick Start

Open the demo page in a web browser:

https://covao.github.io/VibeScratch/vibescratch.html

You can also download `vibescratch.html` and open it directly in any modern web browser — no installation or server required.

## Features

### Panels

* **PALETTE** — left panel for source Markdown blocks; supports Block, Text, and Preview modes
* **Block Editor** — right panel for composing your document; supports Block, Text, and Preview modes
* Resizable panel divider, collapsible sidebar, and fullscreen mode
* Each panel has an **Import** button (file picker or drag-and-drop `.md` / `.txt` files)

### Block Editing

* Drag and drop blocks from the PALETTE into the Block Editor
* Drag blocks within the same panel to reorder them
* Heading blocks carry their entire sub-section when moved
* Collapse / expand heading sections with the arrow toggle
* Hierarchical nesting displayed visually (indented guide lines)
* Supports headings H1–H6, paragraphs, lists, code blocks, and quotes
* Edit any block text inline (contenteditable)
* Add blocks using the `+` bar at the bottom of each panel

### List Blocks

* Reorder list items by drag and drop within a list block
* Drag a list item from the PALETTE directly into a list block in the editor
* Drop a list block onto another list block to merge them
* Add or delete individual list items inline (Enter / Backspace)

### Markdown

* Parses standard Markdown: `#`–`######` headings, `-` / `*` lists, ` ``` ` and `~~~` code fences, `>` blockquotes
* **Text mode** — edit raw Markdown; changes apply automatically when switching back to Block mode
* **Preview mode** — rendered HTML preview of the current content
* **Export** — save the Block Editor content as a `.md` file

### Block Actions (hover to reveal)

* **Duplicate** — copy a block (and its children) directly below
* **Copy text** — copies the block's Markdown text to the clipboard; heading blocks include their full sub-section
* **Delete** — remove a block

### Undo / Redo

* **Undo** button in the title bar (or `Ctrl+Z` / `Cmd+Z`)
* **Redo** button in the title bar (or `Ctrl+Y` / `Ctrl+Shift+Z`)
* Undo/Redo history covers all Block Editor changes: add, delete, duplicate, move, import, and clear

### Block Editor Toolbar

* **Copy All** — copies the entire Block Editor content as Markdown
* **Clear** — clears all blocks in the editor (undoable)
* **Import** — import a Markdown file into the editor

## Requirements

* A modern web browser (Chrome, Edge, Firefox, or Safari — latest recommended)
* JavaScript enabled

## Usage

1. Open `vibescratch.html` in a browser.
2. The **PALETTE** (left panel) contains your source blocks. Type or import Markdown in Text mode, then switch to Block mode.
3. Drag blocks from the PALETTE into the **Block Editor** (right panel) to build your document.
4. Edit block text inline, reorder by dragging, or use the block action buttons (hover to reveal).
5. Switch to **Text** or **Preview** mode in either panel as needed.
6. Use **Export** to save the Block Editor content as a Markdown file.

## Implementation

* Single HTML file — no build step, no dependencies, no server required
* HTML / CSS / JavaScript only
* System fonts (no external font loading)
* Drag-and-drop built on the HTML5 Drag and Drop API
* Markdown parsing and serialization implemented from scratch
