# kishui-video-host

Video assets for [kishui.com](https://kishui.com), served via jsDelivr CDN.
Cafe24 FTP blocks `.mp4` uploads, so the home hero videos are hosted here.

> **DO NOT DELETE, RENAME, OR MAKE THIS REPOSITORY PRIVATE.**
> The live site loads these files directly — any of those breaks the home page videos.

## Files in use

| File | Size | Where | Shown on |
| --- | --- | --- | --- |
| `hero-orin-003.mp4` | 1920×1080, 22.0 s | Home hero, slide 1 (subway) | landscape screens (PC) |
| `hero-orin-003-m.mp4` | 608×1080, 22.0 s | Home hero, slide 1 (subway) | portrait screens (mobile, portrait tablet) |
| `hero-orin-001.mp4` | 1920×1080, 34.9 s | Home hero, slide 2 (close-up) | landscape screens (PC) |
| `hero-orin-001-m.mp4` | 608×1080, 34.9 s | Home hero, slide 2 (close-up) | portrait screens (mobile, portrait tablet) |

Each slide uses two sources:

```html
<source media="(orientation: landscape)" src=".../hero-orin-00X.mp4" type="video/mp4">
<source src=".../hero-orin-00X-m.mp4" type="video/mp4">
```

`-m` files are 9:16 crops of the same 1080p master that follow the subject, so both versions have the same length.

## URL form

```
https://cdn.jsdelivr.net/gh/wuftcorp/kishui-video-host@main/FILENAME
```

## Replacing a video

1. Upload the new file under a **new file name** — jsDelivr caches `@main` for up to 12 h and browsers for 7 days, so overwriting a name shows the old video for a long time.
2. Update the URL in the site skin.
3. Keep the old file until the site no longer references it.
