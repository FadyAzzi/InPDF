<h1 align="center">InPDF</h1>

<p align="center">
  <strong>A PDF viewer and editor for Windows that edits the real page, not a layer on top of it.</strong>
</p>

<p align="center">
  <img alt="version" src="https://img.shields.io/badge/version-0.0.1-1fa8a0">
  <img alt="platform" src="https://img.shields.io/badge/Windows-10%20%7C%2011-0078d4">
  <img alt="dependencies" src="https://img.shields.io/badge/dependencies-none-brightgreen">
  <img alt="offline" src="https://img.shields.io/badge/works-offline-555">
</p>

---

## What it is

Most free PDF tools let you annotate a page but not change it. InPDF edits the
document itself: click any text and retype it, drag an image somewhere else, drop
in a signature or a date.

Those edits are written as **real page content**, reusing the document's own font
wherever it can, so they print, search and copy like text that was always there
rather than sitting in an annotation layer that other readers may or may not
honour.

It also handles scans. Windows' built-in OCR makes a scanned page searchable, and
because a scanned word is pixels rather than text, InPDF covers it with the paper
colour sampled from the page around it and draws your replacement on top, so the
correction matches the paper instead of being a white rectangle.

Everything is undoable, including page operations, and a History panel shows what
has changed and lets you reopen a watermark or a header to adjust it.

---

## Download

Grab the latest **`InPDFInstaller.exe`** from the
[Releases page](https://github.com/FadyAzzi/InPDF/releases) or [Direct Link](https://github.com/FadyAzzi/InPDF/releases/latest/download/InPDFInstaller.zip
).

Run it and follow the wizard. Administrator rights are required, because the
installer registers the PDF file type for all users.

**Requirements:** Windows 10 or 11, 64-bit. Nothing else.

There is no Python to install, no runtime, no OCR engine to download. The
installer carries everything InPDF needs. It works with no internet connection.

---

## Features

### Reading

- Continuous, single-page, facing and facing-continuous layouts
- Zoom to page, to width, or to a fixed level
- **Night mode** inverts the page for reading in the dark
- **Read mode** hides everything but the page, with a bar that reappears when you
  reach for the top edge
- Side panel with thumbnails, bookmarks, comments and search results
- Bookmarks can be renamed, deleted, and dragged to nest into a hierarchy
- Rotate the view without changing the document

### Editing

- Click any text to edit it in place
- Change font, size, bold, italic, colour and alignment as you type
- Move and resize images and objects; hold `Shift` on a corner to keep the shape
- Text that outgrows its original bounds becomes a movable box rather than being
  clipped or dropped

### Inserting

Choose what you want first, then click where it goes.

- **Text boxes** - drag out a box and type
- **Signatures** - draw, type or import once, then reuse
- **Today's date** - one click, in any of six formats, changeable after placing
- **Pictures** - click to place at a sensible size, or drag to size it yourself
- **Links** - make any area clickable, to a web address or another page
- Blank pages, pages from another PDF, and bookmarks
- Watermarks, headers and footers, page numbers, Bates numbering and page
  backgrounds, each reopenable later to adjust

### Signatures

Draw with the mouse, type in a handwriting-style font, or import an image. Saved
signatures are listed with previews and can be renamed or deleted. One stays
loaded after placing, so you can initial every page of a contract without
reopening the picker.

### Comments and markup

- Highlight, underline, strike through, squiggly underline
- Sticky notes and a freehand pen
- All 14 standard PDF rubber stamps (Approved, Draft, Confidential, Final, ...)
- **Export comments** as a text file that quotes the words actually marked up,
  with the page and the line number on that page
- **Flatten** bakes markup into the page when a document is going out

### Shapes and measurement

- Rectangles, ovals, lines, arrows, polygons and connected lines
- Measure distance, perimeter, area and angle
- Calibrate the scale against a length you know, so readings come out in
  real-world units

### Pages and assembly

Rotate, duplicate, delete, extract, split, combine and crop. Reordering pages
keeps every InPDF edit attached to the page it belongs to.

### Protection

- **True redaction** - destroys the content underneath rather than drawing a black
  box over it. Mark an area, or find and redact every occurrence of a phrase,
  then apply.
- **Password protection**, with separate passwords for opening the document and
  for changing what readers are allowed to do
- **Remove hidden information** - metadata, attachments and scripts, before a file
  leaves your hands

### Conversion and comparison

- **OCR** a scan using the engine built into Windows
- **Fill in forms**, and flatten the filled values
- **Compare** two PDFs and get a report of what differs
- **Export** to images, plain text, Word, HTML or CSV
- **Print**, with page range and scaling

### Windows integration

- Registers as a PDF handler, so InPDF appears in *Open with* and in
  *Settings > Default apps*
- Drag a PDF onto the window to open it
- Double-click a PDF to open it, once InPDF is your default

---

## Making InPDF your default PDF app

Windows protects the `.pdf` association with a per-user hash, so no installer can
change your default silently. That is by design, and it applies to every PDF
application, not just this one.

What InPDF can do is register itself properly so it appears in the list. You then
choose it once:

1. In InPDF, go to **Tools > Settings** and click **Open Default apps**
2. Find `.pdf` and pick **InPDF**

---

## Keyboard shortcuts

### File and edit

| Shortcut | Action |
| --- | --- |
| `Ctrl+O` | Open |
| `Ctrl+N` | New blank document |
| `Ctrl+S` | Save |
| `Ctrl+Shift+S` | Save as |
| `Ctrl+W` | Close document |
| `Ctrl+P` | Print |
| `Ctrl+Z` | Undo |
| `Ctrl+Y` / `Ctrl+Shift+Z` | Redo |
| `Ctrl+C` | Copy selected text |
| `Ctrl+A` | Select all text |

### Navigate and view

| Shortcut | Action |
| --- | --- |
| `Ctrl+F` | Focus the search box |
| `F3` / `Shift+F3` | Next / previous match |
| `Page Down` / `Page Up` | Next / previous page |
| `Ctrl+Home` / `Ctrl+End` | First / last page |
| `Ctrl` `+` / `Ctrl` `-` | Zoom in / out |
| `Ctrl+0` | Fit width |
| `F11` | Read mode |
| `Ctrl+Shift+N` | Night mode |
| `Esc` | Cancel the current action |

### Tools

| Key | Tool |
| --- | --- |
| `V` | Select |
| `E` | Edit text |
| `B` | Text box |
| `G` | Signature |
| `D` | Today's date |
| `I` | Picture |
| `H` | Highlight |
| `N` | Sticky note |
| `P` | Freehand pen |

---

## Privacy

InPDF opens your documents locally and never uploads them. It works with no
internet connection at all.

The only network request it ever makes is an optional check for a newer version,
which you can switch off in Settings.

Its own settings and saved signatures live in `%LOCALAPPDATA%\InPDF`. InPDF keeps
an activity log of what it did, never of what your documents contain; the log is
encrypted with a key only your Windows account can unseal, holds the last 30 days,
and can be read or cleared from Settings.

---

## Built with

[PyMuPDF](https://github.com/pymupdf/PyMuPDF) for PDF reading and writing,
[Pillow](https://python-pillow.org/) for images, Tkinter for the interface, and
the OCR engine built into Windows. Packaged with
[Inno Setup](https://jrsoftware.org/isinfo.php).

Building from source is covered in [BUILDING.md](BUILDING.md).

---

## Author

**Fady Azzi**

Copyright © 2026 Fady Azzi. All rights reserved.


NOTE:
==
Some Anti-Viruses or EDRs might block the download of the exe file due to the packaging and not having an Signed Authority certificate. You can Download the zip file as a workaround.

Please download the latest exe or zip version from the right side section "Releases", or use below direct links.

Direct link to the exe is: 
https://github.com/FadyAzzi/InPDF/releases/latest/download/InPDFInstaller.exe

Direct link to the zip is: 
https://github.com/FadyAzzi/InPDF/releases/latest/download/InPDFInstaller.zip
