# 51Sec MM

51Sec MM is a lightweight, single-page video player that can be deployed as a
static website. The interface, styles, and player logic are kept in one HTML
file; no server-side runtime, package installation, or build step is required.

## Project goals

This repository's owner-requested scope is:

1. Include a license, copyright notice, and explicit 51Sec ownership statement.
2. Document the project, its features, and how to use and deploy it.
3. Support desktop and mobile devices with responsive controls and video
   playback.
4. Keep the deployable application in a single HTML file, without a framework,
   build system, or server-side application code.
5. Include the pause-with-image viewing break and display-ad features inspired
   by `51sec/xjj`, while keeping this project independently implemented.
6. Keep the interface compatible with current Chrome, Microsoft Edge, and
   Firefox releases.
7. Present a modern, clean layout with clear controls that are easy to use.

## Features

- Responsive video playback for desktop, tablet, and mobile screens, including
  portrait and landscape layouts, using video aspect ratio and viewport-aware
  sizing.
- Ten selectable video-source endpoints, with a custom URL option. The three
  sources added from XJJ include plain-text API resolution (PF129 and WPON Girl)
  and a JSON API resolved through XJJ's media proxy (Jiejie UK).
- Direct playback for common video files (`.mp4`, `.webm`, `.ogg`, and `.m3u8`)
  when supported by the browser. Other URLs are passed to the selected source
  when that source supports custom URL forwarding.
- Optional automatic playback of the next video and a manual Next control.
- A break after every 10 videos, with a rotating image and Continue/Stop actions.
- Responsive Google AdSense display advertising and ad-block detection.
- A dismissible, non-blocking ad-block notice instead of a full-screen lockout.
- Keyboard-operable controls and support for browser zoom on mobile devices.
- A clear visual hierarchy, readable contrast, visible focus states, and
  touch-friendly controls.
- Social links and a copyright/ownership notice for 51Sec.

## Browser support

The page uses standard HTML, CSS, and browser JavaScript APIs supported by
current Chrome, Edge, and Firefox. Responsive layout includes viewport-unit
fallbacks for browsers that do not support the newer small-viewport unit.
Playback of a particular media format or third-party source still depends on
browser codec support, source availability, and the source's HTTPS/CORS policy.

## Run or deploy

Open `index.html` in a modern browser, or publish this repository with any
static-site host (for example, GitHub Pages). Use an HTTPS host for the best
compatibility with mobile browsers and third-party media endpoints. There is no
build step.

## Use the player

1. Select a video source and choose **Switch** to load from it.
2. Choose **Next** to request another video from the selected source.
3. Paste a direct video URL and choose **Load**. Non-direct URLs are forwarded
   only by sources that support custom URL forwarding; the added PF129, WPON
   Girl, and Jiejie UK sources accept direct video URLs only.
4. Toggle **Auto: On/Off** to control automatic playback when a video ends.
5. After 10 videos have started, the player pauses at the end of the current
   video and displays a break image. Choose **Continue** to reset the counter
   and load the next video, or **Stop** to close the break.

The video and break-image endpoints are third-party services and may change,
become unavailable, or apply their own terms. Some listed endpoints use HTTP;
modern HTTPS pages may block those requests as mixed content.
The added PF129, WPON Girl, and Jiejie UK sources also rely on third-party
proxies; their availability, response format, and terms are outside this
project's control.

## Advertising and analytics

The page includes a responsive AdSense display unit and the existing
advertising, consent, and analytics integrations. Ad delivery depends on the
provider, account approval, user region/consent, and any browser content
blocker. The current AdSense publisher and slot IDs are in `index.html`; update
them if the account or unit changes. Review each provider's policies and
privacy requirements before deployment.

## Ownership and license

51Sec owns and maintains this project and its original code and branding.
Third-party video sources, media, advertising, analytics, and linked services
remain subject to their respective owners' terms and are not relicensed by this
repository.

Copyright (c) 2026 51Sec. The project source is distributed under the MIT
License; see [LICENSE](LICENSE).
