# demos

Standalone HTML files hosted on GitHub Pages at https://demos.exitdoorgames.com.

## Adding a demo

Drop a self-contained `.html` file into the repo (root or any subfolder), commit, and push to `main`:

```sh
cp ~/Downloads/my-demo.html .
git add my-demo.html && git commit -m "Add my-demo" && git push
```

It will be live within a minute or so at `https://demos.exitdoorgames.com/my-demo.html`
(subfolders map directly: `games/foo.html` → `/games/foo.html`).

The home page (`index.html`) automatically lists every `.html` file in the repo.

## Notes

- `CNAME` sets the custom domain — don't delete it.
- `.nojekyll` makes Pages serve files as-is (no Jekyll processing).
- The repo is public, so every file here is publicly visible.
