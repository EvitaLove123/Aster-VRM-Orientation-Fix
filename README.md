# Aster VRM Orientation Fix

An Android-first, browser-based VRM orientation preview tool.

## Current build

- Loads local VRM 0.x / VRM 1.0 files with `@pixiv/three-vrm`.
- 3D preview with grid and XYZ axes.
- Preview-only X/Y/Z rotation controls and quick rotation presets.
- Preview-only ground alignment and centering.
- Displays approximate model dimensions and file size.
- Does not upload the selected model.

## Important limitations

This is an initial preview build, not a complete VRM repair/exporter yet.

- Rotation, centering and ground alignment currently affect only the preview scene.
- The original VRM bytes are not rewritten and no corrected VRM is exported.
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
