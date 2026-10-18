# Royal Islamic Wedding Invitation Website

## Quick start
1. Extract the ZIP.
2. Open `index.html` in a modern browser to preview.
3. Tap **এডিটর খুলুন** to customize. Tap **Save Changes** to save in this browser.
4. For public hosting, upload `index.html` to a GitHub repository and enable GitHub Pages (Settings → Pages → Deploy from a branch → `main` → `/ (root)`).

## Important limitations of this starter
- This is a static, frontend-only version. Browser localStorage is per browser/device, not a cloud database.
- The editor is not secured by authentication. Do not treat `?admin=1` or a hidden editor as security.
- Image and audio uploads use local browser preview only. They are not uploaded to a server and are not automatically available to guests.
- Guest names can be placed in the URL with `?guest=Name`; this is simple URL personalization, not a private guest database.
- For secure admin login, shared edits/media, reliable unique guest links, and permanent data, connect Firebase Authentication + Firestore + Firebase Storage (with security rules) or another backend.
- The default Google Maps URL is a general Chandina search based on the supplied example, not a verified venue pin. Replace it with the exact venue URL before publishing.
- The supplied Hijri date is kept exactly as entered. A warning is displayed because the Hijri/Gregorian pairing may need verification; it is never automatically changed.
- Google Fonts and html2canvas are loaded from external CDNs, so internet is required for those features. If PNG export fails, use browser Print → Save as PDF.

## Publish with GitHub Pages
1. Create/sign in to GitHub.
2. Create a new repository, for example `royal-islamic-wedding`.
3. Upload `index.html` (and this README if desired) to the repository root.
4. Open **Settings → Pages**.
5. Under Build and deployment, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then Save.
6. Wait for GitHub Pages to publish and open the URL shown on the Pages settings screen.
7. Share only the published public URL. A copied local-preview URL is not a public website.

## Suggested production architecture
- Frontend: this invitation page, deployed on GitHub Pages or Firebase Hosting.
- Authentication: Firebase Authentication for owner-only access.
- Data: Firestore document for invitation fields and theme.
- Media: Firebase Storage for background image and audio.
- Security: Firestore/Storage rules allowing only the authenticated owner to write; public read access only to the published invitation data and media.
- Personalized links: a unique invitation ID or guest token resolved by the backend, with no admin credentials in guest URLs.
