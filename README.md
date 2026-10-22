# OmenTracker — Daily Routine & Habit Streaks

A mobile-friendly, installable habit tracker built with plain HTML, CSS, and JavaScript. There are no npm packages and no account is required.

## Features

- Today dashboard with checkable routine items and daily progress.
- Add, edit, and delete habits, with icons, categories, and personal targets.
- Current and best streaks, weekly bars, and a 30-day activity grid.
- Saves check-ins in the browser using `localStorage`.
- Responsive layout for laptops and phones; PWA manifest and offline shell cache included.

## Run it in VS Code on Windows

1. Download and extract `OMENTRACKER_App.zip`.
2. Open VS Code.
3. Choose **File → Open Folder...** and select the extracted `omentracker-app` folder.
4. Open `index.html` and start a local web server. One simple option is to open the VS Code terminal (**Terminal → New Terminal**) and run:

   ```powershell
   py -m http.server 5500
   ```

5. On the laptop, open `http://localhost:5500` in Chrome or Edge.
6. Keep the terminal running while you use the local server. Press **Ctrl+C** in the terminal to stop it.

You can also open `index.html` directly in a browser for basic use, but the service worker/offline shell and PWA install features require a web server.

## Try it on your phone

### Quick local test on the same Wi-Fi

1. Connect your phone and laptop to the same Wi-Fi network.
2. Find the laptop's IPv4 address by running `ipconfig` in Windows Terminal.
3. Start the server with:

   ```powershell
   py -m http.server 5500 --bind 0.0.0.0
   ```

4. On your phone, open `http://YOUR-LAPTOP-IP:5500` (replace the placeholder with the laptop's IPv4 address). If Windows Firewall asks, allow access on your private network.

This local HTTP address is for testing. Some mobile browsers do not allow installation or offline service workers on a local-network HTTP address.

### Install it on your phone

For a proper installable app shortcut, publish the folder to a static HTTPS host such as GitHub Pages. Then:

- **Android:** open the HTTPS site in Chrome, tap the browser menu, and select **Install app** or **Add to Home screen**.
- **iPhone:** open the HTTPS site in Safari, tap **Share**, then **Add to Home Screen**.

## Important data note

Your data is stored only in the browser/device where you use the app. Your laptop and phone will have separate check-ins; this starter version does not have cloud sync, user accounts, or automated reminder notifications. Export/backup and cross-device sync can be added later.

## Files

- `index.html` — app layout, styling, and application logic.
- `manifest.webmanifest` — installable app metadata.
- `sw.js` — cache for the basic offline app shell.
- `icon.svg` — app icon.
