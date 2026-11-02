# MV Dugar Group — email signature generator

Static site. No build step, no server.

## Files

- `index.html` — the generator staff use
- `config.json` — divisions, brands, offices, layout and wording
- `logos/` — one PNG per logo, named by its key

## First time

1. Put these files at the **top level** of the repository, not inside a folder.
2. Settings -> Pages -> Source: *Deploy from a branch*, branch `main`, folder `/ (root)`.
3. Wait a minute, then open the URL GitHub shows you.

## Changing anything afterwards

Open the admin page, make the change, press **Publish settings**. It commits
`config.json` for you and the live page picks it up on the next load.

If you'd rather not give the admin a token, press **Just config.json** instead
and replace that one file by hand.

`index.html` only needs re-uploading if the admin itself has been rebuilt.
Adding or replacing a logo also uploads a PNG into `logos/` — use **Publish
everything** so the filenames match.

## Notes

- GitHub Pages is public on free accounts. No staff details are stored anywhere;
  each person fills their own in, in their browser.
- If a change doesn't show, hard-refresh. GitHub caches for about ten minutes.
- `index.html` keeps a copy of the settings inside it, so if `config.json` is
  ever missing or broken the page still works on the last built-in version.
