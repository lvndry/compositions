# compositions

Public collection of single-file HTML **compositions** made with
[jazz](https://jazz-cli.vercel.app). Each composition is one self-contained
`.html` file — inline CSS/JS, no build step, no CDN, works offline.

## Browse

- [Index](https://lvndry.github.io/compositions/) — all public compositions, with URLs
- [How the Jazz composition tool works](https://lvndry.github.io/compositions/composition-tool.html)

## Structure

```
/
├── index.html              ← landing page (listing of everything public)
├── composition-tool.html   ← flat file, published at /composition-tool.html
└── <slug>/index.html       ← optional folder form, published at /<slug>/
```

Both flat files and folders work — Cloudflare/GitHub Pages serve whichever
exists. Newer compositions use the folder form so each can carry an
`og.png` social card alongside.

## Hosting

GitHub Pages, published from `main`:
`https://lvndry.github.io/compositions/<path>`

## Publishing

Compositions are published from a jazz session with the `publish_composition`
tool (public visibility → this repo, GitHub Pages host). The tool writes the
page, renders the Jazz-branded `og.png`, commits and pushes; Pages picks it up
within a minute. Private compositions live in a separate, non-public repo so
this index never leaks their titles.
