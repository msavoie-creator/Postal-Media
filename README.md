# postalmedia.io

Static site for Postal Media. No build step, no framework, no dependencies:
plain HTML and one stylesheet, so it deploys anywhere and loads instantly.

```
/                      studio: the stamp and the roster
/content/              Content's own page (its colours, not the studio's)
/content/privacy/      Content's privacy policy, the App Store link
/plateau/              Plateau, in production
/support/              one address, no ticket system
/assets/css/site.css   the whole design system
/assets/brand/         logos: postal-media.svg, content-icon.png, plateau-icon.svg
/assets/img/           app screenshots (iPhone 1320×2868, iPad, Mac, Apple TV)
CNAME                  postalmedia.io
```

## Deploying

Copy these files into the repo already serving GitHub Pages and push. `CNAME`
is included; delete it if the custom domain is configured in repo settings
instead, so the two don't fight.

## The design, in one paragraph

One black ground (`#0A0A0A`) on every page, and one accent at a time: the
studio's red (`#EE4C44`, sampled from the stamp), Content's orange
(`#FF7E00`), Plateau's gold (`#E0AC2E`). `<html data-world="content">` or
`data-world="plateau"` swaps only the accent; the background never changes,
so each app still has its own world without the site flipping between light
and dark as you move around. The fun is in scale and motion: very large,
very heavy type; stickers that sit slightly
off-square; the word that changes in Content's headline; hollow outline type
for the closing line. Adding a third app is one `[data-world]` line in the
CSS and one card on the homepage.

Content's page is built as a numbered index of the ten things it does that
other trackers don't, rather than a general overview. That list is the
sales pitch.

## Fonts

System stacks, deliberately: nothing to download, nothing to go wrong, and no
third-party request. The weight and tracking are doing the work. If you ever
licence a condensed grotesk for the display type, swapping `--sans` in
`:root` is the only change needed.

## Editing the privacy policy

The page was generated from `Docs/PRIVACY_POLICY.md` in the Content repo, which
remains the source of truth. Regenerate rather than hand-editing the HTML, so
the policy and the app can't drift apart.

## Local preview

```
python3 -m http.server 4321 --directory .
```
