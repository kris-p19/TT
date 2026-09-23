# Repository guidance

- This is a two-page static site with no package manifest, build, test, lint, format, or typecheck commands. Do not invent npm-based workflows; changes can only be verified by inspecting and manually viewing the HTML.
- `index.html` is the default page and loads Tailwind CSS from its Play CDN; its theme overrides are inline in `<head>`. `unocss.html` is a separate experimental alternative using the UnoCSS runtime, not a build output of `index.html`.
- The pages share no source files or assets. Keep each implementation self-contained, and verify both files after an edit rather than assuming a change to one affects the other.
- Rendering requires network access to the Tailwind/UnoCSS and Google Fonts CDNs. Font settings are duplicated: update each page's Google Fonts link and its local font stack together.