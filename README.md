# Portfolio — Astro

A responsive portfolio inspired by the supplied homepage template and the supplied Bone / Merlot / Olive / Midnight Blue / Tobacco / Graphite palette.

## Features

- Single-page portfolio with four main scroll sections:
  - Home
  - Works
  - Contact
  - Blog
- My Story is a horizontal-scroll section reached from Home.
- Works, My Story and Blog use horizontal snap-scrolling.
- Horizontal cards work with mouse/trackpad and touch swipes.
- Responsive mobile layout.
- Hamburger navigation on phones.
- Active desktop navigation follows the current section.
- Accessible semantic sections and navigation.
- No UI framework required.

## Run locally

```bash
npm install
npm run dev
```

Then open the local Astro URL shown in the terminal.

## GitHub Pages

1. Create a GitHub repository, for example `portfolio`.
2. Change `site` and `base` in `astro.config.mjs`.

Example:

```js
export default defineConfig({
  site: "https://YOUR_USERNAME.github.io",
  base: "/portfolio"
});
```

If the repository itself is `YOUR_USERNAME.github.io`, use:

```js
export default defineConfig({
  site: "https://YOUR_USERNAME.github.io",
  base: "/"
});
```

3. Add a GitHub Actions workflow that runs `npm run build` and deploys `dist/` to GitHub Pages.

## What to edit first

Open `src/pages/index.astro` and replace:

- `YOUR NAME`
- `YOUR_EMAIL@example.com`
- LinkedIn / GitHub `#` links
- CV link
- portrait placeholder
- project information
- blog information

The colors are defined at the top of `src/styles/global.css`:

```css
--bone: #E6E0D6;
--merlot: #4B1E23;
--olive: #6B6F4E;
--midnight: #1C2430;
--tobacco: #8A5A2B;
--graphite: #121212;
```

## Adding your image

Put your portrait in:

`public/images/profile.jpg`

Then replace the placeholder inside `.portrait-placeholder` with:

```astro
<img src="/YOUR_REPOSITORY_NAME/images/profile.jpg" alt="Your name" />
```

For a root GitHub Pages repository (`YOUR_USERNAME.github.io`), use `/images/profile.jpg`.
