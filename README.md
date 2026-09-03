# Wall Display OTA

Over-the-air update channel for the custom Shelly Wall Display app (`com.kurucz.walldisplay`).

The app polls `version.json`; when its `versionCode` is higher than the installed one it downloads
`walldisplay.apk` and launches the system installer.

Set the display's update URL (Beállítások → Frissítés) to:

```
https://raw.githubusercontent.com/u4mzu4/walldisplay-ota/main/
```

The APK here is built **without** the baked-in Wi-Fi credentials, so it contains no secrets.
To publish a new version: bump `versionCode`/`versionName` in the app, build, copy the APK here as
`walldisplay.apk`, update `version.json`, and push.
