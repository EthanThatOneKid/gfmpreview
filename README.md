# gfmpreview

Preview
[GitHub-flavored markdown (GFM)](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
files right in your browser — no backend needed.

[![screenshot of gfmpreview landing page](https://github.com/user-attachments/assets/f768697a-9005-4a59-9368-aef03d0d387a)](https://ethanthatonekid.github.io/gfmpreview)

## How it works

Paste a GitHub blob URL (or prepend this site's URL to one). The page
converts it to a `raw.githubusercontent.com` URL, fetches the markdown
with `fetch()`, and renders it client-side with
[`marked`](https://github.com/markedjs/marked), sanitized by
[`DOMPurify`](https://github.com/cure53/DOMPurify) and styled with
[`github-markdown-css`](https://github.com/sindresorhus/github-markdown-css).

## Development

No build step and no server. Serve the folder with any static file server:

```sh
npx serve .
```

or

```sh
python3 -m http.server
```

## Deployment

Deploy as static hosting (e.g. GitHub Pages). `404.html` is a copy of
`index.html` so the `/<blob-url>` scheme keeps working on hosts without
SPA rewrites.

## References

- Inspired by [htmlpreview.github.io](https://htmlpreview.github.io/)

---

Developed with 💖 by [**@EthanThatOneKid**](https://etok.codes/)
