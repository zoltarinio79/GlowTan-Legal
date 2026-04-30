# [APP NAME] — Legal

Privacy Policy and Terms of Service for the [APP NAME] iOS app, hosted via GitHub Pages.

## Setup

1. Create a new public repo on GitHub (e.g. `appname-legal`).
2. Drop these files into the repo and commit.
3. Go to **Settings → Pages**.
4. Under "Source", select your default branch (`main`) and the `/ (root)` folder. Save.
5. Wait ~1 minute. Your site will be live at:
   - `https://USERNAME.github.io/appname-legal/`
   - `https://USERNAME.github.io/appname-legal/privacy`
   - `https://USERNAME.github.io/appname-legal/terms`

## Before publishing — fill in the placeholders

Search for these placeholders in `privacy.md` and `terms.md` and replace them:

- `[APP NAME]` — your app's name
- `[YOUR NAME OR COMPANY]` — the legal entity behind the app
- `[YOUR CONTACT EMAIL]` — support email
- `[DATE]` — effective and last-updated dates
- `[NAME OF API, e.g. OpenWeatherMap / Apple WeatherKit]` — your UV/weather data provider
- `[URL TO PROVIDER POLICY]` — link to that provider's privacy policy
- `[Cyprus / your jurisdiction]` — governing law jurisdiction

## App Store Connect

In App Store Connect → App Information → paste the URLs into:

- **Privacy Policy URL** → `https://USERNAME.github.io/appname-legal/privacy`
- **License Agreement / EULA** (optional, custom) → `https://USERNAME.github.io/appname-legal/terms`
