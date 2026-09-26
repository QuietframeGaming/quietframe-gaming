# Quietframe Gaming Website

Files:
- `index.html` — the website
- `quietframe-channel-logo.png` — your channel logo

## Updating your subscriber count / videos

No GitHub Action, no API key, nothing to configure. Open `index.html` in a text
editor, find this block near the top of the `<script>` section:

```js
const CHANNEL_DATA = {
    subscribers: 22,
    videoCount: 15,
    updatedLabel: "LAST UPDATED MANUALLY",
    videos: [
        { id: "2mva9Qv4nzg", title: "Quietframe Gaming", description: "Latest gaming adventure." },
        ...
    ]
};
```

Change the numbers, save, and re-upload `index.html` to GitHub. That's it —
the subscriber countdown bar recalculates automatically from whatever number
you put in `subscribers`.

To swap in a new video, replace one of the `id` values with the video ID from
its YouTube URL (the part after `watch?v=`), and update its `title` /
`description`.

## Deploying

Push `index.html` and `quietframe-channel-logo.png` to a GitHub repo, then
turn on GitHub Pages for it (Settings → Pages → set source to your main
branch). No secrets, no Actions tab, no workflow file needed.
