# Android home-screen installation

This is a static website. Publish the entire repository, including
`manifest.webmanifest` and the `icons` folder, on an HTTPS host. The manifest uses
relative paths so it also works when hosted in a subfolder, such as a GitHub Pages
project site. Open the site's directory URL (with a trailing slash) or `index.html`.

To install on Android:

1. Remove the old home-screen shortcut, or uninstall the previous installed web app.
2. Open the updated HTTPS website in Chrome and reload it.
3. Open Chrome's three-dot menu and select **Add to Home screen**, then **Install**
   (some Chrome versions show **Install app** directly).
4. Launch the newly installed app from the home screen.

The manifest requests fullscreen mode, which removes Chrome's address bar and
browser controls when launched as an installed app. Android may still display
system controls temporarily, and browser/device support determines the final
presentation. Opening the URL in a normal Chrome tab still shows browser controls.

If Chrome offers only a regular shortcut, check that the deployed manifest and both
PNG icons load successfully over HTTPS, then try again. A local `file://` page or
an HTTP LAN address does not meet secure-origin installation requirements.

No service worker or offline caching is included; the site requires a network
connection to load.
