# CleanYourTV for TizenBrew — Q70C fork

A fast, remote-first launcher-style home screen for Samsung Tizen TVs that runs
inside [TizenBrew](https://github.com/reisxd/TizenBrew).

This fork is tuned for a **Samsung Q70C / Tizen 9** TV:

- **Built-in app list fallback.** Stock TizenBrew does not declare the
  `application.info` privilege, so `tizen.application.getAppsInfo()` is refused
  on retail TVs. The module then falls back to a built-in list of installed app
  IDs (TizenTube, Jellyfin, Moonlight, Stremio, IPTV, VLC, Plex, NuvioTV,
  Reiverr, AniLiberty, KickTV, TizenFeed, FCast, RTSP, HackTV, OpenTTD, Chiaki,
  Fladder, HyperTizen, Overscan, Tailscale, plus stock YouTube/Netflix/Prime/
  Apple TV/Internet/SmartThings) and launches them with
  `tizen.application.launch()` — which TizenBrew **does** declare.
- English UI labels and date.
- Green pins/unpins a favorite (max 7), Red/Blue page, Yellow refresh,
  OK launches, Back returns to TizenBrew.
- 7x3 pagination; no heavy blur.

## Install through TizenBrew

Module Manager → **Add GitHub Module** → enter:

```
securityvisions/cleanyourtv-tizen
```

## Limit

Samsung retail Tizen does not allow a third-party app to replace the Home/Smart
Hub button. CleanYourTV runs as a launcher-like module inside TizenBrew.
