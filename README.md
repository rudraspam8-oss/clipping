# ClipForge
Installable web app (PWA) that turns a video up to 30 min into 5-10 captioned 9:16 shorts (15-30 s). No paid APIs.

## Deploy free on Cloudflare Pages
1. Push these files to your GitHub repo (root of the repo).
2. Cloudflare dashboard > Workers & Pages > Create > Pages > Connect to Git > pick the repo.
3. Framework: None. Build command: empty. Output directory: `/`. Deploy.
4. Open the URL on your phone > Share/Menu > Add to Home Screen.

## Notes
- Accounts, styles and history are stored on the device (localStorage). Passwords are PBKDF2-hashed. This is not a server login: it does not sync across phones.
- Captions: Whisper tiny.en via transformers.js (about 40 MB, downloaded once). Shorts are recorded in real time, so a 25 s short takes about 25 s to render. Keep the screen on.
- Saving: iPhone/Android share sheet (choose Save Video). Falls back to a download.
