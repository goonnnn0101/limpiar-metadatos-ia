# Metadata Cleaner

A browser-only tool that strips metadata and AI traces from your files.

Nothing is uploaded: every file is processed locally in your browser.

## Supported formats

| Format | What gets cleaned |
|--------|-------------------|
| **Word** (`.docx`) | Author, software, dates, title, keywords. The text is not modified. |
| **Excel** (`.xlsx`) | Same as Word. Cell contents are left untouched. |
| **PowerPoint** (`.pptx`) | Same as Word. Slides are left untouched. |
| **PDF** | Title, author, creator, producer, keywords and dates. |
| **Images** | EXIF, GPS, C2PA, prompts and other embedded metadata (by re-encoding). |
| **Text** (`.txt`, `.md`, …) | Invisible characters and common AI filler phrases. |

## Usage

1. Open [`index.html`](index.html) in your browser (or clone the repo and open it locally).
2. Drop one or more files onto the page.
3. For each file you can set:
   - the output name
   - the creation date
   - the modification date
4. Optionally, use the top bar to apply the same dates to every file or to add the `clean_` prefix.
5. Click **Clean and download**.

## Features

- Per-file controls (independent name and dates)
- Apply dates to every file in the list at once
- Automatic `clean_` prefix
- Responsive interface
- No server: a single HTML file, with [JSZip](https://stuk.github.io/jszip/) and [pdf-lib](https://pdf-lib.js.org/) loaded from a CDN

## Limitations

- **Statistical watermarks** from models such as Claude or Gemini (a bias in word choice) are not metadata and are not removed; they can only be diluted by rewriting the text.
- For Office documents only the metadata is cleaned; the content is kept intact on purpose.
- Images are re-encoded, so JPEGs are recompressed (quality 95) and HEIC/AVIF files are saved as PNG.

## Privacy

All processing happens in the browser. No file is sent to any server.

## License

Free to use. Contributions are welcome.
