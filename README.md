# Place Pins

A map-based app for pinning places to eat, stay, see and shop. Installable as a PWA and works offline.

Places are saved on each device. Turn on sync (below) to see the same places on all your devices.

## Turn on sync (Firebase, free)
1. Create a project at https://console.firebase.google.com (Analytics not needed).
2. **Build → Authentication → Get started → Email/Password → Enable.** (Needed behind the scenes, even though you never type an email.)
3. **Authentication → Settings → Authorized domains → Add domain:** `<your-username>.github.io`
4. **Build → Firestore Database → Create database** (production mode, any location). Then on the **Rules** tab paste the contents of `firestore.rules` and **Publish**.
5. **Project settings (gear) → Your apps → Web (`</>`)**, register the app, copy the `firebaseConfig` object.
6. Paste it into `firebase-config.js` as `window.FIREBASE_CONFIG = { ... };` and commit.
7. Open the app → **Sign in to sync** → type a password (8+ characters) → type it again to create it. On other devices, type the same password.

There's no email or username: the password alone is the key to your places, so pick one that's hard to guess. There's no reset if you forget it.

## Install
Open the GitHub Pages URL, then:
- **iPhone/iPad (Safari):** Share → Add to Home Screen
- **Android (Chrome):** menu → Install app
- **Desktop (Chrome/Edge):** install icon in the address bar

## Updating
After changing `index.html`, bump `VERSION` in `sw.js` so installed copies refresh their cache.
