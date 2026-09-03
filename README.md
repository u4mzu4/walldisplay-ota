# Wall Display OTA

Over-the-air update channel for the custom Shelly Wall Display app (`com.kurucz.walldisplay`).

- **GitHub Releases** — what the display checks: `https://api.github.com/repos/u4mzu4/walldisplay-ota/releases/latest`.
  The release **tag is the versionCode** (e.g. `30`); the first `.apk` asset is downloaded and installed silently
  (the app runs as a privileged system app on the display).
- **`main` branch** — always carries the current `walldisplay.apk` and `version.json` too (archive + raw fallback:
  `https://raw.githubusercontent.com/u4mzu4/walldisplay-ota/main/`).

The APKs here are built **without** the baked-in Wi-Fi credentials, so they contain no secrets.

Publishing (from the app repo): `.\tools\release.ps1 -VersionCode N -VersionName X -Push` — builds, creates the
release, updates `main`, and pushes the update to the display over the LAN.
