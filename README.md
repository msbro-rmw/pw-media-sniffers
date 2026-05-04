# PW Media Sniffer

A GitHub Pages tool to capture media URLs (m3u8, mp4, mpd, pdf) from **pwthor.live** using a bookmarklet.

## How It Works

1. Visit the GitHub Pages site
2. Copy the bookmarklet from the site
3. Save it as a bookmark in your browser
4. Go to **pwthor.live**, open a video/PDF
5. Tap the bookmark → URLs auto-captured
6. Hit **Save Data** → downloads a `.txt` file with all URLs

## Features

- 📡 Auto-sniffs m3u8, mp4, mpd, pdf URLs
- 🔢 Sequence numbered captures
- 💾 Save all URLs to `.txt` file
- ↺ Restart with confirmation
- 📋 Copy individual URLs
- 🔗 Open URLs directly

## GitHub Repository Structure

```
pw-media-sniffer/
├── index.html      ← Landing page
├── sniffer.html    ← Main tool (open this)
└── README.md
```

## Setup on GitHub Pages

1. Create a new **public** repository named `pw-media-sniffer`
2. Upload `index.html`, `sniffer.html`, and `README.md`
3. Go to **Settings → Pages → Source → main branch**
4. Your site: `https://yourusername.github.io/pw-media-sniffer/sniffer.html`

## Note

The bookmarklet works by injecting JavaScript into pwthor.live that intercepts XHR/fetch/video requests and stores found media URLs in localStorage. The sniffer page polls localStorage every 1.5 seconds to pick up new URLs.
