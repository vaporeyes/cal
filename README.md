# Cal

A single-page printable calendar that displays an entire year at a glance. Based on [Neatnik's Calendar](https://neatnik.net/calendar), converted to client-side JavaScript with additional features.

## Usage

Open `index.html` in a browser. Print the page (landscape orientation recommended) to get a full year on one sheet.

### URL Parameters

| Parameter | Description |
|-----------|-------------|
| `year` | Display a specific year (e.g., `?year=2026`). Defaults to current year. |
| `layout` | Set to `aligned-weekdays` to align days by weekday position across months. |
| `sofshavua` | Highlight Friday/Saturday as weekends instead of Saturday/Sunday. |

**Examples:**

- `index.html?year=2026`
- `index.html?layout=aligned-weekdays`
- `index.html?sofshavua`
- `index.html?year=2026&sofshavua`

## Running with Redbean

[Redbean](https://redbean.dev/) is a single-file distributable web server. You can package this calendar into a standalone executable:

```bash
# Download redbean from https://redbean.dev/#download
# and rename it to redbean.com (or whatever)
chmod +x redbean.com

# ensure index.html is readable
chmod 644 index.html

# Add the calendar files
zip redbean.com index.html

# Run it
./redbean.com -p 8080
```

Then open `http://localhost:8080` in your browser.

The resulting `redbean.com` file is a self-contained executable that works on Linux, macOS, Windows, FreeBSD, OpenBSD, and NetBSD.

## License

MIT License

Original work: Copyright (c) 2025 Neatnik LLC
Modifications: Copyright (c) 2025 Vaporeyes

See [index.html](index.html) for full license text.
