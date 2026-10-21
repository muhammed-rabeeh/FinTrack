# FinTrack — Installable Mobile PWA Package

## Folder Structure
```
fintrack-pwa/
├── index.html                 # Main FinTrack app wired to manifest.json & sw.js
├── manifest.json              # Web App Manifest (standalone display, shortcuts, icons)
├── sw.js                      # Offline-first Service Worker (precaches shell + CDNs)
└── icons/
    ├── icon-192.png           # 192x192 home screen icon (Android & standard)
    ├── icon-512.png           # 512x512 splash & store icon
    ├── icon-maskable-512.png  # 512x512 adaptive maskable icon for Android
    └── apple-touch-icon.png   # 180x180 iOS home screen icon
```

## How to Install on Mobile Devices
Mobile browsers (Chrome on Android and Safari on iOS) require PWAs to be served over **HTTPS** (or `http://localhost` during testing) with separate `manifest.json` and `sw.js` files:

1. **Deploy for Free in 30 Seconds**:
   - **Netlify Drop**: Drag and drop the `fintrack-pwa` folder onto `https://app.netlify.com/drop`.
   - **GitHub Pages / Vercel**: Push this folder to a GitHub repository and enable GitHub Pages.
2. **Install on Android (Chrome)**:
   - Open your hosted HTTPS URL in Chrome on Android.
   - Tap the **Install App** button inside FinTrack (`Budgets -> Install App`) or tap Chrome's menu (`⋮`) -> **Install app**.
   - Android compiles a WebAPK and adds **FinTrack** to your app drawer with long-press shortcuts for **Scan Google Pay QR** and **Group Pay**.
3. **Install on iOS (Safari)**:
   - Open the HTTPS URL in Safari on iPhone, tap the **Share** icon, and select **Add to Home Screen**.
