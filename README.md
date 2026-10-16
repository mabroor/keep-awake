# Caffeine — Keep Awake

A single-page web app that stops your screen from sleeping or dimming, using the browser's native [Screen Wake Lock API](https://developer.mozilla.org/en-US/docs/Web/API/Screen_Wake_Lock_API).

**Live:** https://mabroor.github.io/keep-awake/

## Features

- Timed sessions (15m, 30m, 1h, 2h) or indefinite mode
- Re-acquires the lock when you return to the tab
- Shows a log of the last five sessions

## Limitations

- The lock only holds while the tab is **visible**. If you switch tabs, minimise the window, or lock the device, the screen can sleep. When you come back, the page asks for the lock again.
- It keeps the **screen** awake. It doesn't stop the OS from sleeping on its own (for example, when the lid is closed).
- It needs a secure context (HTTPS or localhost). It works in current Chrome, Edge, Safari 16.4+, and Firefox 126+.

## Run locally

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

There is no build step. Tailwind CSS, Alpine.js, and Lucide load from CDNs, each pinned to a fixed version.
