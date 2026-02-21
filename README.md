# Figure 3.4 Deep Zoom Viewer (GitHub Pages)

This project is a static OpenSeadragon viewer for **Figure 3.4** hosted on GitHub Pages.

It loads:
- `tiles/figure3_4.dzi`
- `tiles/figure3_4_files/` (tile pyramid folder)

No server-side code, frameworks, or build tools are required.

## Project Structure

```text
/ (repo root)
  index.html
  README.md
  tiles/
    figure3_4.dzi
    figure3_4_files/
      0/
      1/
      2/
      ...
```

## A) Prepare Figure 3.4 as a DZI

1. Export **Figure 3.4** from your PDF as a high-resolution PNG.
2. Generate a Deep Zoom package using one of these tools:
   - Deep Zoom Tools
   - Zoomify
   - Online DZI generator
3. Ensure the output is named exactly:
   - `figure3_4.dzi`
   - `figure3_4_files/`
4. Place both outputs inside the `tiles/` folder.

Final expected paths:
- `tiles/figure3_4.dzi`
- `tiles/figure3_4_files/` (with all tile levels inside)

## B) Upload the Project to GitHub

1. Create a new GitHub repository.
2. Upload these files/folders to the repo root:
   - `index.html`
   - `README.md`
   - `tiles/` (including `figure3_4.dzi` and `figure3_4_files/`)
3. Commit and push.

## C) Enable GitHub Pages

You can use either method below:

### Option 1: Deploy from `main` branch
1. Open your repository on GitHub.
2. Go to **Settings -> Pages**.
3. Under **Build and deployment**, set:
   - **Source**: Deploy from a branch
   - **Branch**: `main` / `(root)`
4. Save and wait for deployment.

### Option 2: GitHub Actions source
1. Go to **Settings -> Pages**.
2. Set **Source** to **GitHub Actions**.
3. Add a Pages workflow if prompted.
4. Wait for deployment.

## D) Access the Viewer

Your viewer URL will be:

`https://USERNAME.github.io/REPO/`

Example:

`https://janedoe.github.io/figure3-4-viewer/`

## E) Link to the Viewer from a PDF

1. Open your PDF editor.
2. Add a hyperlink on the Figure 3.4 caption, callout, or icon.
3. Point the link to your GitHub Pages URL.
4. Save/export the PDF.

When readers click the link, they will open the interactive deep-zoom viewer in their browser.

## Troubleshooting

- If the viewer is blank, verify file names and case exactly match:
  - `figure3_4.dzi`
  - `figure3_4_files/`
- If zoom opens but tiles fail, re-upload the full `figure3_4_files/` directory tree.
- Keep `index.html` at repo root so GitHub Pages serves it as the site homepage.
