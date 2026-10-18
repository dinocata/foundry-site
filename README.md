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
