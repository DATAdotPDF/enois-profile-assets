# Énois IA — Profile Assets

An independent banner for **Pedro D. Ferreira (.pdf)** on [Énois IA](https://enois.ia.br/perfil/dotpdf). This repository contains only this profile's visual assets. It does not change the profile repository or portfolio.

## Public URLs

- Demo: https://datadotpdf.github.io/enois-profile-assets/
- Background: https://datadotpdf.github.io/enois-profile-assets/assets/manga-background.webp
- Copyable snippet: https://github.com/DATAdotPDF/enois-profile-assets/blob/main/cover-snippet.html

## Files

```text
enois-profile-assets/
├── README.md
├── index.html
├── cover-snippet.html
├── assets/
│   ├── manga-background.webp
│   └── cover.css
├── .gitignore
└── .nojekyll
```

`index.html` demonstrates the banner. `cover-snippet.html` contains the standalone banner with scoped CSS and absolute HTTPS asset URLs. The demo uses `assets/cover.css`, which must stay identical to the snippet's inline stylesheet. No JavaScript, frameworks, fonts, embeds, or Base64 resources are required.

## Use on Énois IA

Copy the entire contents of `cover-snippet.html` into the platform's HTML banner editor. Save and inspect the result on desktop and mobile. The profile itself has not been edited by this project.

The platform must retain `<style>`, `<audio>`, `<source>` and inline `<svg>` markup. Its sanitizer, content security policy and banner height limits have not been tested in an authenticated editor. If any of these are removed, the standalone demo can work while the profile does not. Do not describe a saved profile as validated until it has been checked there.

## Layout and artwork

The supplied 995 × 306 monochrome artwork was converted to lossless WebP without resizing, retouching or regeneration. Decoded RGBA pixels match the original exactly. Original PNG: 566,227 bytes. WebP: 210,918 bytes, a 62.75% reduction.

The full image remains in the asset. The banner uses `object-fit: cover`, so its visible crop varies with the container. It has a 4:1 aspect ratio at wide desktop sizes and extra height on smaller screens to preserve readable text and native audio controls. The SVG Log Pose points straight north and is hidden from assistive technologies because it is decorative.

## Live radio

The source is https://radio.animeamaze.net:8443/AnimeAMAZE64 with MIME type `audio/aac`. It uses native HTML5 play/pause controls, `preload="none"`, and no autoplay, iframe or new window.

On 2026-10-17, an HTTPS GET returned HTTP 200, `Content-Type: audio/aac`, Icecast metadata with 64 kb/s, two channels and 44,100 Hz. A bounded 15-second probe received 183,879 bytes. Its timeout was intentional because the live stream has no finite end.

In the Chromium-based in-app browser, playback advanced beyond 159 seconds, `readyState` was 3, no media error was present, and `canPlayType('audio/aac')` returned `probably`. Native play and pause were exercised. This is not a claim of validation on Safari, Firefox, every operating system, or inside Énois IA. AAC availability depends on the browser and operating system. The remote stream can also become unavailable or be blocked by network policy, port 8443 restrictions or the destination site's CSP. The supplied source was preserved.

## Update

1. Replace `assets/manga-background.webp` with a new user-approved image. Keep the name or update both HTML files with the new URL. Update the image's width and height attributes if its dimensions change.
2. Edit the banner markup in both HTML files. Keep the exact name and description unless the owner requests a change.
3. Edit `assets/cover.css` and copy its complete contents into the snippet's `<style>` element. All selectors must remain under `.enois-pdf-cover`.
4. Commit to `main`. GitHub Pages serves the root directory of that branch. Wait for deployment and verify the public image and demo.
5. Copy the revised snippet into Énois IA and check the saved profile.

## Checks and scope

The project is tested at desktop and mobile widths for text overlap, overflow, image loading and visible north marking. Native keyboard controls are checked separately from mouse input. The snippet is inspected for local paths, relative external URLs, Base64, scripts, iframes and unscoped CSS.

Only this new repository is in scope. Temporary tools, source attachments, browser evidence and audio probes are not published. The original artwork's ownership is not assigned or licensed by this repository.
