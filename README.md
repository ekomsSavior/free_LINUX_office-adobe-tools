# Free Linux Office / Adobe Tools

> Replace subscriptions. Retain control. 

This repository is a practical field guide for replacing paid Microsoft Office and Adobe software with free, open-source Linux tools.

The objective is not to imitate a corporate software ecosystem perfectly. The objective is to build a professional workflow that can create presentations, reports, spreadsheets, illustrations, photographs, videos, magazines, zines, and print-ready PDFs without recurring license fees.

This guide is written primarily for **Ubuntu**, **Kali Linux**, **Debian**, and other Debian-based distributions.

Repository:

```text
https://github.com/ekomsSavior/free_LINUX_office-adobe-tools/
```

---

## The Replacement Stack

| Paid software or task | Free Linux replacement | Primary use |
|---|---|---|
| Microsoft Word | LibreOffice Writer | Documents, reports, letters, manuscripts |
| Microsoft Excel | LibreOffice Calc | Spreadsheets, tables, formulas, charts |
| Microsoft PowerPoint | LibreOffice Impress | Conference talks, slide decks, presentations |
| Microsoft Access | LibreOffice Base | Desktop databases |
| Adobe Photoshop | GIMP | Photo editing, compositing, raster graphics |
| Adobe Illustrator | Inkscape | Vector art, logos, diagrams, stickers |
| Adobe Fresco | Krita | Digital painting, illustration, concept art |
| Adobe InDesign | Scribus | Magazines, zines, books, flyers, print layouts |
| Adobe Lightroom | darktable | RAW photography and photo organization |
| Adobe Premiere Pro | Kdenlive | Video editing and production |
| Adobe Acrobat Reader | Okular | PDF reading, annotation, forms, signatures |
| Basic Adobe Acrobat editing | LibreOffice Draw | Basic PDF element and page editing |

These applications are alternatives, not exact clones. Proprietary formats such as `.docx`, `.pptx`, `.ai`, `.psd`, and complex PDFs may not render identically in every application. Keep a native Linux master file and export copies for delivery.

---

# 1. Install the Complete Stack

Update the package index:

```bash
sudo apt update
```

Install everything covered by this guide:

```bash
sudo apt install libreoffice gimp inkscape krita scribus kdenlive darktable okular -y
```

After installation, open the application menu and search for the program by name.

You can also launch each tool from a terminal:

```bash
libreoffice
gimp
inkscape
krita
scribus
kdenlive
darktable
okular
```

## Install Only What You Need

Office and PDF tools:

```bash
sudo apt install libreoffice okular -y
```

Graphic design and publishing tools:

```bash
sudo apt install gimp inkscape krita scribus -y
```

Photography and video tools:

```bash
sudo apt install darktable kdenlive -y
```

---

# 2. LibreOffice

**Replaces:** Microsoft Office

LibreOffice is a complete open-source office suite. It includes several separate applications that work together.

| LibreOffice application | Replaces | Purpose |
|---|---|---|
| Writer | Microsoft Word | Documents and reports |
| Calc | Microsoft Excel | Spreadsheets and data |
| Impress | Microsoft PowerPoint | Presentations |
| Draw | Basic Visio and PDF editing | Diagrams and page editing |
| Base | Microsoft Access | Databases |
| Math | Equation Editor | Mathematical formulas |

## Install

```bash
sudo apt update
sudo apt install libreoffice -y
```

## Launch

Open the entire suite:

```bash
libreoffice
```

Open a specific application:

```bash
libreoffice --writer
libreoffice --calc
libreoffice --impress
libreoffice --draw
```

## Writer: Documents and Reports

Use Writer for:

- Security reports
- Vulnerability disclosures
- Research papers
- Speaker biographies
- Conference handouts
- Letters and nonprofit documents

Basic workflow:

1. Open **LibreOffice Writer**.
2. Create a new document.
3. Use **Styles** for headings instead of manually resizing every heading.
4. Insert images with **Insert > Image**.
5. Add page numbers, headers, or footers through the **Insert** menu.
6. Save the editable master as `.odt`.
7. Export a delivery copy as `.pdf` or save a compatibility copy as `.docx`.

Export a PDF:

```text
File > Export As > Export as PDF
```

## Calc: Spreadsheets and Data

Use Calc for:

- Budgets
- Conference expenses
- Research inventories
- Vulnerability tracking
- Contact lists
- Charts and tables
- Nonprofit bookkeeping exports

Basic workflow:

1. Open **LibreOffice Calc**.
2. Enter labels in the first row.
3. Enter data underneath each label.
4. Use formulas beginning with `=`.
5. Select data and use **Insert > Chart** to create a chart.
6. Save the master as `.ods`.
7. Save a compatibility copy as `.xlsx` when necessary.

Example formula:

```text
=SUM(B2:B20)
```

## Impress: PowerPoint Presentations

Use Impress for:

- Cybersecurity conference presentations
- Technical training
- Nonprofit talks
- Workshop slides
- Speaker decks

Basic workflow:

1. Open **LibreOffice Impress**.
2. Select a blank presentation or template.
3. Set the slide dimensions before building the deck.
4. Use the master slide to control repeated fonts, logos, and backgrounds.
5. Add text, images, diagrams, video, and speaker notes.
6. Save the editable master as `.odp`.
7. Save a compatibility copy as `.pptx`.
8. Export a PDF backup before presenting.

Launch Impress directly:

```bash
libreoffice --impress
```

Save as PowerPoint:

```text
File > Save As
File type: PowerPoint 2007–365 (.pptx)
```

Recommended conference workflow:

```text
presentation-master.odp
presentation-delivery.pptx
presentation-backup.pdf
```

Always open the exported `.pptx` and PDF before the conference. Check fonts, image placement, animations, embedded media, and line breaks.

## Draw: Diagrams and Basic PDF Editing

Use Draw for:

- Network diagrams
- Process diagrams
- Simple vector graphics
- Basic PDF edits
- Rearranging imported document elements

Open a PDF:

```bash
libreoffice --draw document.pdf
```

Draw can import many PDFs and expose text or graphic elements for editing. Complex PDFs may import imperfectly. It is useful for basic corrections, but it is not a complete replacement for every Acrobat Pro feature.

---

# 3. GIMP

**Replaces:** Adobe Photoshop

GIMP is a raster image editor. Raster images are built from pixels, making GIMP appropriate for photographs, screenshots, textures, social graphics, and image composites.

## Install

```bash
sudo apt update
sudo apt install gimp -y
```

## Launch

```bash
gimp
```

## Use GIMP For

- Editing photographs
- Removing or replacing backgrounds
- Cropping screenshots
- Creating layered graphics
- Adjusting brightness and color
- Preparing images for presentations
- Exporting PNG and JPEG files
- Building web and social-media graphics

## Basic Workflow

1. Open GIMP.
2. Select **File > Open** and choose an image.
3. Duplicate important layers before destructive edits.
4. Use the crop, selection, paint, transform, text, and color tools.
5. Save the editable master as `.xcf`.
6. Export the final image as `.png`, `.jpg`, `.webp`, or another delivery format.

Export an image:

```text
File > Export As
```

Recommended file strategy:

```text
conference-art-master.xcf
conference-art-transparent.png
conference-art-web.jpg
```

Do not treat JPEG as an editable master. JPEG compression discards information every time the image is repeatedly exported.

---

# 4. Inkscape

**Replaces:** Adobe Illustrator

Inkscape is a vector graphics editor. Vector artwork is built from mathematical paths instead of fixed pixels, allowing logos and illustrations to scale without becoming blurry.

## Install

```bash
sudo apt update
sudo apt install inkscape -y
```

## Launch

```bash
inkscape
```

## Use Inkscape For

- Logos
- Stickers
- Icons
- Diagrams
- Technical illustrations
- T-shirt graphics
- Posters
- SVG artwork
- Presentation assets
- Laser-cutting or plotting designs

## Basic Workflow

1. Open Inkscape.
2. Set the page size through the document properties.
3. Use shapes, paths, text, fills, strokes, and alignment tools.
4. Convert final text to paths only when a printer specifically requires it.
5. Save the editable master as `.svg`.
6. Export a `.png` for web use or a `.pdf` for print and sharing.

Recommended file strategy:

```text
logo-master.svg
logo-print.pdf
logo-transparent.png
```

For reusable logos, preserve the original SVG. A PNG is only an exported copy.

---

# 5. Krita

**Replaces:** Adobe Fresco and many digital-painting workflows

Krita is built for digital painting and illustration. It is especially useful with a drawing tablet, but it also works with a mouse.

## Install

```bash
sudo apt update
sudo apt install krita -y
```

## Launch

```bash
krita
```

## Use Krita For

- Digital paintings
- Character art
- Concept art
- Cyberpunk illustrations
- Comics
- Textures
- Background paintings
- Frame-by-frame 2D animation
- Artwork for posters and zines

## Basic Workflow

1. Open Krita.
2. Create a document at the final required dimensions.
3. Use separate layers for sketches, line art, color, shading, and effects.
4. Select brushes from the brush preset panel.
5. Save the editable master as `.kra`.
6. Export the final artwork as `.png`, `.jpg`, `.tiff`, or `.pdf`.

Recommended file strategy:

```text
illustration-master.kra
illustration-print.tiff
illustration-web.png
```

Krita is generally the better choice for drawing and painting. GIMP is generally the better choice for photo manipulation and pixel-level image editing.

---

# 6. Scribus

**Replaces:** Adobe InDesign

Scribus is a desktop-publishing application. It is designed for assembling text, images, typography, pages, bleeds, margins, and print-ready PDFs.

This is the primary tool in this stack for magazines, books, zines, brochures, and professional page layouts.

## Install

```bash
sudo apt update
sudo apt install scribus -y
```

## Launch

```bash
scribus
```

## Use Scribus For

- Magazines
- Cybersecurity zines
- Books
- Conference programs
- Flyers
- Posters
- Brochures
- Multi-page reports
- Print-ready PDF files

## Basic Zine Workflow

1. Open Scribus.
2. Select **File > New**.
3. Set the document unit, page size, orientation, margins, page count, and bleed.
4. Create master pages for repeated headers, backgrounds, and page elements.
5. Insert text frames for written content.
6. Insert image frames for artwork and photographs.
7. Link text frames when an article continues across columns or pages.
8. Use paragraph and character styles for consistent typography.
9. Run the preflight verifier before export.
10. Export a print-ready PDF using the printer's required settings.

For a 6-by-9-inch zine:

```text
Width: 6 inches
Height: 9 inches
Orientation: Portrait
```

Ask the printer for its required bleed, color profile, PDF standard, and image-resolution requirements before final export.

Save the Scribus master as `.sla`.

Recommended project structure:

```text
zine-project/
├── document/
│   └── issue-master.sla
├── images/
├── fonts/
├── exports/
│   ├── issue-proof.pdf
│   └── issue-print.pdf
└── text/
```

Do not move or rename linked images after placing them in Scribus unless you intend to relink them.

---

# 7. darktable

**Replaces:** Adobe Lightroom

darktable is a photography workflow and RAW-development application. It is intended for organizing photographs and making controlled exposure, color, tone, lens, and detail adjustments.

## Install

```bash
sudo apt update
sudo apt install darktable -y
```

## Launch

```bash
darktable
```

## Use darktable For

- RAW camera files
- Headshot processing
- Exposure correction
- White-balance correction
- Color grading
- Lens correction
- Photo organization
- Batch exports
- Preparing images for print or web

## Basic Workflow

1. Open darktable.
2. Import a photograph or folder.
3. Use the **lighttable** view to organize and select images.
4. Use the **darkroom** view to edit the selected image.
5. Adjust exposure, white balance, contrast, color, crop, and detail.
6. Export the finished image as JPEG, PNG, TIFF, or another required format.

Keep original RAW files. Exported images are delivery copies, not replacements for the camera originals.

---

# 8. Kdenlive

**Replaces:** Adobe Premiere Pro

Kdenlive is a non-linear video editor based on the KDE ecosystem and FFmpeg.

## Install

```bash
sudo apt update
sudo apt install kdenlive -y
```

## Launch

```bash
kdenlive
```

## Use Kdenlive For

- Conference recordings
- Training videos
- Interviews
- Social clips
- Screen recordings
- Titles and subtitles
- Multi-track audio and video editing
- Basic color correction
- Rendered MP4 delivery files

## Basic Workflow

1. Open Kdenlive.
2. Create a project using the correct resolution and frame rate.
3. Import video, audio, images, and music into the project bin.
4. Drag clips onto the timeline.
5. Cut and arrange clips.
6. Add transitions, titles, effects, and audio adjustments.
7. Save the editable project.
8. Render the final video.

A common delivery format is:

```text
MP4
H.264 video
AAC audio
```

Save the editable project separately from rendered video files.

Recommended project structure:

```text
video-project/
├── project/
├── footage/
├── audio/
├── graphics/
├── proxies/
└── renders/
```

Video editing consumes significant CPU, memory, and storage. Proxy clips can improve performance when editing high-resolution footage on a laptop.

---

# 9. Okular

**Replaces:** Adobe Acrobat Reader

Okular is a document viewer from KDE. It can open PDFs and many other document formats.

## Install

```bash
sudo apt update
sudo apt install okular -y
```

## Launch

```bash
okular
```

Open a specific document:

```bash
okular report.pdf
```

## Use Okular For

- Reading PDFs
- Highlighting text
- Adding annotations
- Reviewing documents
- Filling supported forms
- Presenting PDF slides
- Viewing EPUB, images, comics, and other supported formats

Okular is primarily a viewer and annotation tool. Use LibreOffice Draw for basic PDF element editing and Scribus for rebuilding professional page layouts.

---

# 10. Professional Workflows

## Cybersecurity Conference Presentation

```text
Krita, GIMP, or Inkscape
        |
        v
Create artwork, diagrams, and visual assets
        |
        v
LibreOffice Impress
        |
        v
Save master as ODP
        |
        +--> Export PPTX compatibility copy
        |
        +--> Export PDF emergency backup
```

Before presenting:

- Test the deck on the actual presentation computer.
- Embed or package required media.
- Verify fonts.
- Carry the `.odp`, `.pptx`, and `.pdf` versions.
- Keep a copy on local storage and a separate removable drive.
- Do not depend entirely on conference Wi-Fi.

## Zine or Magazine

```text
Writer or Markdown
        |
        v
Edit article text
        |
        v
GIMP, Inkscape, and Krita
        |
        v
Create and prepare artwork
        |
        v
Scribus
        |
        v
Preflight and export print-ready PDF
```

## Social Graphic or Poster

```text
Inkscape for vector layout
GIMP for photographs and textures
Krita for original illustration
```

## Photography

```text
Camera RAW files
        |
        v
darktable
        |
        v
Export TIFF for print or JPEG/PNG for web
```

## Video

```text
Footage, screen recordings, audio, and graphics
        |
        v
Kdenlive
        |
        v
Render MP4
```

---

# 11. Native Masters and Delivery Copies

Preserve an editable native master. Export separate copies for clients, conferences, printers, websites, or collaborators.

| Tool | Native master | Common delivery formats |
|---|---|---|
| Writer | `.odt` | `.pdf`, `.docx` |
| Calc | `.ods` | `.xlsx`, `.pdf`, `.csv` |
| Impress | `.odp` | `.pptx`, `.pdf` |
| GIMP | `.xcf` | `.png`, `.jpg`, `.webp` |
| Inkscape | `.svg` | `.pdf`, `.png` |
| Krita | `.kra` | `.png`, `.tiff`, `.jpg` |
| Scribus | `.sla` | `.pdf` |
| Kdenlive | `.kdenlive` | `.mp4`, `.webm` |
| darktable | Original RAW plus edit data | `.jpg`, `.png`, `.tiff` |

A delivery file is not the master file.

---

# 12. Microsoft Office Compatibility

LibreOffice can open and save many Microsoft Office formats, including:

```text
.doc
.docx
.xls
.xlsx
.ppt
.pptx
```

Compatibility is strong for ordinary documents, but complex layouts, macros, fonts, SmartArt, animations, transitions, and embedded objects may change.

Recommended practice:

1. Work in LibreOffice's native format.
2. Save a separate Microsoft-format copy.
3. Reopen the Microsoft-format copy.
4. Inspect every page or slide.
5. Export a PDF reference.
6. Send both the requested format and the PDF when appropriate.

---

# 13. Troubleshooting

## Package Not Found

Refresh package information:

```bash
sudo apt update
```

Then retry the installation.

## Broken Dependencies

```bash
sudo apt --fix-broken install
sudo apt update
```

Retry the original installation command afterward.

## Check Whether a Program Is Installed

```bash
which libreoffice
which gimp
which inkscape
which krita
which scribus
which kdenlive
which darktable
which okular
```

## Check the Installed Version

```bash
libreoffice --version
gimp --version
inkscape --version
krita --version
scribus --version
kdenlive --version
darktable --version
okular --version
```

Some graphical applications may not support identical command-line version flags across every release. The application's **Help > About** screen is the fallback.

## Remove a Tool

Example:

```bash
sudo apt remove gimp -y
```

Remove the complete stack:

```bash
sudo apt remove libreoffice gimp inkscape krita scribus kdenlive darktable okular -y
sudo apt autoremove -y
```

## Application Does Not Appear in the Menu

Log out and back in, or launch the program from a terminal using its command name.

## Fonts Look Different on Another Computer

The other system may not have the same fonts installed.

Use broadly available fonts, install the required fonts on the presentation system, convert critical logo text to paths in Inkscape, or export a PDF backup.

Do not convert an entire presentation or long document into outlines unless necessary. Outlined text is harder to edit and may reduce accessibility.

---

# 14. Security Notes

Install software from your Linux distribution's repositories or from the project's official distribution channels.

Avoid random installation scripts, unofficial package repositories, pirated software archives, and unknown binary downloads.

Before installing an unfamiliar package, inspect it:

```bash
apt show PACKAGE_NAME
apt-cache policy PACKAGE_NAME
```

Linux removes the subscription gate. It does not remove the need for backups, file verification, controlled updates, and operational discipline.

---

# 15. Official Project Documentation

- [LibreOffice](https://www.libreoffice.org/)
- [GIMP](https://www.gimp.org/)
- [Inkscape](https://inkscape.org/)
- [Krita](https://krita.org/)
- [Scribus](https://www.scribus.net/)
- [darktable](https://www.darktable.org/)
- [Kdenlive](https://kdenlive.org/)
- [Okular](https://okular.kde.org/)

