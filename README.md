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

The home page (`index.html`) automatically shows a tile for every `.html` file in the repo, titled with the page's `<title>`.

To give a demo a preview image, add a JPEG at `thumbs/<same path>.jpg` (e.g. `thumbs/games/foo.jpg` for `games/foo.html`). One way to capture it:

```sh
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --hide-scrollbars \
  --window-size=1200,750 --virtual-time-budget=6000 --screenshot=thumbs/my-demo.png "file://$PWD/my-demo.html"
sips -s format jpeg -s formatOptions 80 --resampleWidth 800 thumbs/my-demo.png --out thumbs/my-demo.jpg && rm thumbs/my-demo.png
```

## Notes

- `CNAME` sets the custom domain — don't delete it.
- `.nojekyll` makes Pages serve files as-is (no Jekyll processing).
- The repo is public, so every file here is publicly visible.
