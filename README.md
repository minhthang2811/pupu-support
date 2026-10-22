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
App Store Connect point at the same three addresses. The app links to the
privacy policy and the support page too, from Me → About (App Review asks for
the privacy policy to be reachable inside the app, guideline 5.1.1).

## Publishing

GitHub Pages builds the root of `main` with Jekyll, using the theme set in
`_config.yml`. Push to `main` and the site rebuilds within a minute or two.
There is no build step of our own: every page is plain Markdown.

## Keeping the privacy policy true

The policy says Pupu makes no network requests of any kind. Pupu is a native
SwiftUI app with no networking code and no third-party SDKs, so that holds as
long as:

- the only way out is a link the user taps in Me → About, which Safari opens;
- icon suggestions keep using Apple's on-device Foundation Models and nothing
  that runs in the cloud;
- reminders stay local notifications, with no push service.

If any of that changes, the privacy policy here, the App Review notes and the
App Privacy answers in App Store Connect have to change together.
