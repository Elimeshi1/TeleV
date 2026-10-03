# telev.app

Website for TeleV, the Telegram app for Android TV: plain HTML/CSS served by
GitHub Pages from `main`, no build step.

```
index.html                          Home page
guide/watch-telegram-on-tv/         "How to watch Telegram on TV" guide
privacy/, terms/, delete-data/, …   Legal pages (linked from Google Play)
privacy-policy.html                 Redirect from the old /privacy-policy URL
sitemap.xml, robots.txt             For search engines
CNAME                               Custom domain (telev.app)
remote-config.json                  Read by the app — see below
```

**`remote-config.json` must stay at the repo root on `main`.** The app fetches it from
`https://raw.githubusercontent.com/Elimeshi1/TeleV/main/remote-config.json` to decide
whether to show the "update required" screen (`minVersionCode`).

## Preview locally

```
python3 -m http.server 8000
```

## When adding a page

Add it to `sitemap.xml`.
