# SketchTool Action

This is a quick & dirty experiment to show `sketchtool` running on GitHub Actions.

## What this does

Whenever a `.sketch` document is pushed or merged to `master`, a GitHub Action will run and:

- Download & install the latest Sketch version
- Run `sketchtool export` to extract all the exportable assets in your document
- Archive all those assets in an `assets.zip` file
- Create a new release in the repo, and attach `assets.zip` to it

All the paths are hardcoded, but the code is trivial enough to modify for your particular needs. See `.github/workflows/sketchtool.yml` for more details.

Huge props to @mathieudutour for his help with the release process.