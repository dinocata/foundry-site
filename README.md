# Foundry website

Privacy and support pages for Foundry by Swift d.o.o. This public repository contains only website files; app source is maintained separately.

## Publish

After reviewing the pages, commit and push the files to `main`. In GitHub, open **Settings → Pages**, select **Deploy from a branch**, then **main / (root)**, and save. Enable HTTPS when available.

Expected URLs:

- https://dinocata.github.io/foundry-site/
- https://dinocata.github.io/foundry-site/privacy/
- https://dinocata.github.io/foundry-site/support/

The pages use plain HTML and CSS, with no build dependencies, JavaScript, tracking, or third-party fonts. Relative links work under the GitHub Pages project path.

## Preview

Run `python3 -m http.server 8765` in this directory, then open http://localhost:8765/.

Update the policy date whenever privacy practices change. Keep provider descriptions aligned with the app and retention statements aligned with production configuration.

## App Store launch checklist

- Publish the contact email update and verify that the home, support, and privacy URLs above load publicly over HTTPS.
- Send a test message to hello@swift.hr and confirm that replies can be sent from that address.
- Confirm the email-provider description in the privacy policy matches the service handling hello@swift.hr.
- Compare the privacy policy with the release build and production Firebase settings: analytics defaults by country and age, consent controls, crash reporting defaults, identifiers, retention, deletion requests, and update checks.
- Match App Store Connect privacy disclosures to the data collected by the app and its third-party SDKs. Confirm the app links to the public privacy and support pages.
- Verify that the backup instructions and Preferences labels match the release app.
- Replace the temporary https://apps.apple.com/ link marked `APP_STORE_URL` in index.html with Foundry’s App Store product URL. Remove the coming-soon placeholder note and verify the product destination before launch.

Do not mark privacy or provider checks complete until verified against the release configuration. Update the privacy policy and its date if those checks require changes.
