HVF Work Order App v5 - Defaults Fix Offline PWA

This version is designed to run offline on iPhone after it is installed from Safari as a Home Screen app.

V5 defaults fix:
- Save Defaults now verifies browser storage.
- Clear reloads saved defaults instead of hard-coded values.
- Added a Load Defaults button and visible defaults status message.
- Built-in HVF logo is no longer unnecessarily saved to browser storage.

How to install on iPhone with GitHub Pages:
1. Upload the contents of this folder to a GitHub repository. index.html must be at the top level of the repository.
2. Turn on GitHub Pages from Settings -> Pages -> Deploy from branch -> main -> / root.
3. Open the GitHub Pages link in Safari on the iPhone.
4. Wait for the page to fully load and show the offline status.
5. Tap Share -> Add to Home Screen.
6. Open the new HVF Work Orders icon once while online.
7. After that, the app shell should open offline. PDF generation and photo attachment run locally on the phone.

Important notes:
- Do not open index.html from the iPhone Files app. Files preview does not reliably run the PDF/share features.
- A service worker only installs from HTTPS, localhost, or 127.0.0.1. It will not install from a plain local file.
- Photos and work order data stay local in the browser/app. Export/save the PDF after each work order.
- iPhone may clear browser storage if the device is low on space, so do not rely on the app as your only record system.

Local desktop testing:
1. Open a terminal in this folder.
2. Run: python -m http.server 8000
3. Open http://localhost:8000 on the desktop.
