# KraveKitchen-Assignment-3
Krave Kitchen is a small Progressive Web App I made to keep track of recipes. You can browse recipes, view them, and “add” new ones (it’s a prototype, so it doesn’t save permanently yet).  

---

### Service Worker
I added a service worker (`service-worker.js`) to make the app work offline. It caches all important files like HTML, CSS, JS, and images, so you can still use the app even without internet.  

### Caching Strategy
- On first load, the service worker caches the essential files:
  - All HTML pages (`index.html`, `recipes.html`, etc.)
  - `style.css`
  - `manifest.json`
  - Images in the `images/` folder
- When the app is offline, it serves files from the cache so the UI still works.

### Manifest File
The `manifest.json` file makes the app installable on devices and determines how it looks:
- **name**: Krave Kitchen    
- **description**: A prototype app to keep track of recipes  
- **icons**: Includes multiple sizes for mobile and desktop  
- **start_url**: Opens the main page (`index.html`)  
- **display**: opens like a normal app without browser bars  
- **background_color & theme_color**: Match the app design  

---

## How to Test
1. Open `index.html` in Chrome.  
2. Open DevTools → Application → Service Workers to check registration.  
3. Go offline in DevTools → refresh → app should still work.  
4. On mobile, try “Add to Home Screen” to install the PWA.  

---

Made by Olivia Becker
