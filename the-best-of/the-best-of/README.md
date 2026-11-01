# The Best Of

A free, open-source site that helps Gen Z founders figure out where to start. Spin the slot machine to land on "The best of [something] [something]" and read a short, curated list. Startup ideas, side hustles, free courses, study techniques, routines, and the tools to get going.

By LīMEN.

## What's in here

```
the-best-of/
├── index.html     # the whole site: markup, styles, list data and script
├── favicon.svg    # gummy bear tab icon
├── vercel.json    # clean URLs and caching headers for Vercel
├── LICENSE        # MIT
└── README.md
```

There's no build step and no dependencies. The site is one static HTML file plus Google Fonts.

## Run it locally

Open `index.html` in a browser, or serve the folder:

```bash
npx serve .
```

## Publish to GitHub

1. Create a new empty repository on GitHub (for example `the-best-of`). Don't add a README or license there; they're already here.
2. In this folder, run:

```bash
git init
git add .
git commit -m "Launch The Best Of"
git branch -M main
git remote add origin https://github.com/<your-username>/the-best-of.git
git push -u origin main
```

## Deploy on Vercel

1. Go to vercel.com, sign in with GitHub, and click **Add New → Project**.
2. Import the `the-best-of` repository.
3. Leave the settings as they are: Framework Preset **Other**, no build command, output directory is the root.
4. Click **Deploy**. You'll get a `*.vercel.app` link in under a minute.
5. Optional: add your own domain under **Project → Settings → Domains**.

Every push to `main` redeploys automatically.

Prefer the command line? Run `npx vercel` in this folder, then `npx vercel --prod`.

## Add or edit a list

All lists live in `index.html`, inside the `LISTS` array in the script. Each list looks like this:

```js
L("Free", "Coding Courses", "Who it's for",
  "keywords people might type, separated by spaces",
  [
    ["Pick name", "https://link.com", "One-line description.", "Best for…"],
    // more picks
  ],
  { lab: "Best for", note: "Optional line shown under the list." }
),
```

- The first two values are the two words on the slot machine.
- The keywords help the "Wah wah, niche taste" screen suggest close lists when someone types a combo that doesn't exist.
- `lab` changes the label under each pick (for example "First step" or "Try"). Leave the last argument out to use "Best for".
- Picks without a link use `""` for the URL.

New adjectives and categories show up on the reels and in the typing suggestions automatically.

## Before you launch

- Check every link and app detail. Plans and prices change.
- Lists about skin, health, calm and money include a short "not medical/financial advice" note. Keep those.

## Contributing

Spotted an outdated pick or want a new list? Open an issue or a pull request.

## License

MIT, see `LICENSE`.
