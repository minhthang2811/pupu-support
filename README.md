# Pupu support site

The public web pages for [Pupu](https://minhthang2811.github.io/pupu-support/),
the iPhone day planner that holds the shape of your day. The app's own code is
in a private repository; this one holds only what App Store Connect links to.

## Pages

| File | URL | App Store Connect field |
|---|---|---|
| `index.md` | https://minhthang2811.github.io/pupu-support/ | Marketing URL |
| `support.md` | https://minhthang2811.github.io/pupu-support/support | Support URL |
| `privacy-policy.md` | https://minhthang2811.github.io/pupu-support/privacy-policy | Privacy Policy URL |

The pages are in English only, so the English and Vietnamese localizations in
App Store Connect point at the same three addresses.

## Publishing

GitHub Pages builds the root of `main` with Jekyll, using the theme set in
`_config.yml`. Push to `main` and the site rebuilds within a minute or two.
There is no build step of our own: every page is plain Markdown.

## Keeping the privacy policy true

The policy says Pupu makes no network requests of any kind. That is true only
while over-the-air updates stay off in the app: `expo-updates` is installed but
has no `updates.url`, so every build ships with updates disabled. If that ever
changes, the privacy policy here, the App Review notes and the App Privacy
answers in App Store Connect have to change together.
