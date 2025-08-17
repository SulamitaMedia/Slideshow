
Flickr Signage Slideshow (Last 7 Days, Techy Collage)
=====================================================

Files:
- index.html  -> Single-file web app (no build step). Just upload to your hosting and open it.

Default configuration (embedded):
- Flickr API key: 4855498d62dbadaf2bd11df6fcdb9f08
- Username: sulamitachurchpdx
- Shows uploads from the last 7 days.
- Multiple photos per slide with a justified, tidy layout that preserves each photo's aspect ratio.
- Techy neon look, subtle scanlines, animated transitions between slides.
- Auto-advance every 12s, auto-refresh feed every 5 minutes.

You can override options via URL parameters:
- rowHeight: target row height in pixels (default 320)  e.g. ?rowHeight=280
- gap: space between photos in pixels (default 16)      e.g. ?gap=12
- duration: slide duration in ms (default 12000)        e.g. ?duration=15000
- refresh: refresh interval in ms (default 300000)      e.g. ?refresh=120000
- shuffle: true/false (default false)                   e.g. ?shuffle=true
- tags: comma-separated tags to filter                  e.g. ?tags=sunday,choir

Examples:
- https://YOUR_DOMAIN/signage/index.html?rowHeight=280&gap=12&duration=15000
- https://YOUR_DOMAIN/signage/index.html?shuffle=true
- https://YOUR_DOMAIN/signage/index.html?tags=sunday,choir

Bluehost Install (cPanel) — Step by Step
----------------------------------------
1) Log in to your Bluehost account and open cPanel.
2) Go to "File Manager".
3) In the left sidebar, click `public_html`. (This is your web root.)
4) Click the "+ Folder" button and create a folder, e.g., `signage`.
5) Open the new `signage` folder, then click "Upload".
6) Upload the `index.html` file from this package.
7) When done, visit: https://YOUR_DOMAIN/signage/index.html
   (Replace YOUR_DOMAIN with your actual domain.)

Optional:
- If you want it at the root domain, upload index.html directly into `public_html` and visit https://YOUR_DOMAIN/.
- To use a subdomain (e.g., signage.YOUR_DOMAIN), create a subdomain in cPanel first, point it to `public_html/signage`, then upload the file there.

Kiosk / Fullscreen Tips
-----------------------
- Press the "Fullscreen" button (or press "F") to enter fullscreen.
- On a signage PC, set the browser to kiosk mode and load the URL at startup.

Troubleshooting
---------------
- If no photos appear, ensure your Flickr API key is valid and that the username exists.
- The app shows only the last 7 days of uploads. If there are no uploads in that period, it will render no photos.
- Network/caching: hold Shift and click Reload in the browser to bypass cache if you updated the file recently.
- Rate limits: The app refreshes every 5 minutes by default. If you hit Flickr rate limits, increase the refresh interval.

Security Note
-------------
This app is client-side and exposes your Flickr API key in the page source. If you need to restrict usage,
create a separate Flickr key just for this signage deployment and rotate if needed.
