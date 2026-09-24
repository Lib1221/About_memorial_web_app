> **Archived.** This repository is kept read-only for reference and to keep the existing GitHub Pages deployment online. Active development happens in [KeneniAdugna](https://github.com/Lib1221/KeneniAdugna); new web builds should be published from that repository's `gh-pages` branch instead of a separate repo.

# Keneni Adugna Memorial (Web Build)

Compiled Flutter web output for **the Keneni Adugna memorial app**. This repository holds the production build (`flutter build web`) and is intended for static hosting such as GitHub Pages. The application source lives in [KeneniAdugna](https://github.com/Lib1221/KeneniAdugna).

Live: [https://lib1221.github.io/About_memorial_web_app/](https://lib1221.github.io/About_memorial_web_app/)

## Contents

```
index.html               # Entry point (base href: /About_memorial_web_app/)
flutter_bootstrap.js     # Flutter web loader
main.dart.js             # Compiled Dart application
flutter_service_worker.js
manifest.json            # PWA manifest
assets/                  # Bundled fonts, images, and Flutter assets
canvaskit/               # CanvasKit renderer
icons/                   # App icons
```

## Serving locally

Any static file server works:

```bash
python -m http.server 8080
# open http://localhost:8080
```

## Rebuilding

From the source repository:

```bash
flutter build web --release --base-href "/About_memorial_web_app/"
```

Then copy the contents of `build/web/` into this repository and push.
