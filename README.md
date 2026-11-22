# capstonemimic.github.io

Stable short links for the capstonemimic org. Print a link (or a QR code of it)
once and change where it points later.

## Add a link

Create `_links/<name>.md`:

```yaml
---
to: https://openreview.net/forum?id=XXXX
---
```

Commit to `main`. About a minute later,
`https://capstonemimic.github.io/<name>/` redirects to that URL.

## Change where a link points

Edit the `to:` line and commit. The short link (and any QR code made from it)
stays the same.

## Notes

- Use lowercase letters, digits and hyphens in names (`tsc-iclr-poster`).
  The name is part of the printed URL, so pick one you'll keep.
- For QR codes, encode the full URL with the trailing slash:
  `https://capstonemimic.github.io/<name>/`.
- Never delete or rename a link that has been printed; just repoint it.
- Redirects are client-side (meta refresh + JavaScript), as GitHub Pages
  can't send HTTP 301s. Browsers and phone QR scanners follow them instantly.
