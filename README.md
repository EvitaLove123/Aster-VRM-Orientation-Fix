# Aster VRM Orientation Fix

An Android-first, browser-based VRM orientation preview tool.

## Current build

- Loads local VRM 0.x / VRM 1.0 files with `@pixiv/three-vrm`.
- 3D preview with grid and XYZ axes.
- X/Y/Z rotation controls and quick rotation presets.
- Ground alignment and centering.
- **Download VRM** exports a new `.vrm` with the current orientation/position adjustment applied as a glTF scene-root transform. Original binary resources and VRM extension data are retained.
- Displays approximate model dimensions and file size.
- Does not upload the selected model.

## Important limitations

This is an early export implementation, not a full VRM repair suite.

- Export preserves the original GLB binary chunks and VRM extension JSON, then adds a parent scene node carrying the current preview transform. It does not rewrite humanoid bones or bake the transform into every mesh.
- Test the exported file in your target apps (Virtual Droid, Napharmonia, VRM Posing Mobile, or Me/v); compatibility is not guaranteed for every importer.
- Automatic orientation detection is heuristic; it cannot reliably infer every character's intended forward/up direction.
- Automatic orientation detection is heuristic; it cannot reliably infer every character's intended forward/up direction.
- Some model-specific import behavior may be caused by the target application rather than the VRM file.

## Run on GitHub Pages

1. Open **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch `main` and folder `/ (root)`, then Save.
4. Open the published Pages URL.

The first load requires an internet connection to retrieve Three.js and three-vrm from jsDelivr. Offline use is not guaranteed in this initial build.

## Files

- `index.html` — application
- `README.md` — project notes

## Privacy

The selected VRM is read locally in the browser. This app does not send model files to a server.
