# Legal pages

Static, host-anywhere copies of the Terms of Service and Privacy Policy.

**Why these exist:** Apple App Store Connect and Google Play Console both require
a publicly reachable **privacy policy URL** in the store listing (Apple also
wants a Terms/EULA link for subscription apps). In-app screens alone don't
satisfy that — the same content also lives in the app at
`trainer-mobile/src/content/legal.ts` (rendered by `/terms` and `/privacy`).

**Keep in sync:** if you edit one side, edit the other. Source of truth is
`trainer-mobile/src/content/legal.ts`.

## Hosting (pick one, all free)

- **GitHub Pages:** push this `legal/` folder to a repo → Settings → Pages →
  deploy from branch. URLs become `https://<user>.github.io/<repo>/terms.html`.
- **Netlify / Vercel:** drag-and-drop the folder; done.
- **Your own domain** (e.g. `https://lifterlog.app/terms`): preferred if you
  buy the domain — matches the defaults already in `trainer-mobile/.env`.

Then put the final URLs in:
- App Store Connect → App Privacy + the EULA/Terms field
- Google Play Console → Store listing → Privacy policy
- `trainer-mobile/.env` → `EXPO_PUBLIC_TERMS_URL` / `EXPO_PUBLIC_PRIVACY_URL`
  (kept for store metadata reference; the app itself renders the bundled copies)

## Before launch

- Have the documents reviewed by a qualified person — they were drafted to
  match what the app actually does, but this is not legal advice.
