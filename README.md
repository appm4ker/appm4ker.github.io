# appm4ker.github.io

Static GitHub Pages website. No build step or dependencies are required.

## Pages

- `/`: appm4ker developer landing page.
- `/voxbrowser/`: Vox Browser app presentation and store links.
- `/voxbrowser/privacy_policy.html`: privacy policy (formerly the root index).
- `/voxbrowser/terms.html`: terms of service.
- `/voxbrowser/support.html`: app support.
- `/styles.css`: shared responsive landing-page styles.
- `/voxbrowser/assets/`: branding and screenshots copied from `browser-flutter/play_store_listing/google_play/`.

Use the new `/voxbrowser/` legal and support URLs in the app store consoles. The root `/privacy_policy.html`, `/terms.html`, and `/support.html` redirect to their new locations for existing links. The root URL now shows the developer landing page, so store listings that used the root URL for privacy must be updated.

Keep `/app-ads.txt` at the domain root for advertising verification.

## Add store links when ready

Edit `voxbrowser/index.html`, in `<section id="download">` near the bottom.

Google Play already links directly to `https://play.google.com/store/apps/details?id=com.appm4ker.voxbrowser`.

Apple and Amazon intentionally have no links yet. Locate the `STORE LINK` comments and replace each corresponding `<span class="store-pending">...</span>` with an anchor using the real listing URL, for example:

```html
<a class="button secondary" href="YOUR_APPLE_APP_STORE_URL">Download on the App Store</a>
<a class="button secondary" href="YOUR_AMAZON_APPSTORE_URL">Get it on Amazon Appstore</a>
```

Replace the example URL values with your direct product URLs. Update the paragraph above the buttons to reflect availability, and remove each completed `STORE LINK` comment. There is no JavaScript configuration or build to update.

## Preview

From this directory run `python -m http.server 8000`, then open `http://localhost:8000/` and `http://localhost:8000/voxbrowser/`.

The presentation uses the 2.1 feature assets and copy from `browser-flutter`. Confirm feature availability against the released store versions before publishing. Legal policy text is preserved; review it separately for changes in app data handling.
