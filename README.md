# Quietframe Gaming Website

Files:
- `index.html` — website
- `quietframe-channel-logo.png` — your existing YouTube channel logo, cropped from your screenshot
- `youtube.json` — feed used by the website
- `.github/workflows/update-youtube.yml` — automatic YouTube updater

## Automatic videos / subscribers
For automatic updates on GitHub Pages, add a GitHub repository secret named:

`YOUTUBE_API_KEY`

The workflow uses your `@QuietframeGaming` handle and updates `youtube.json` every 15 minutes.

The website itself remains static, so the API key is never placed inside `index.html`.
