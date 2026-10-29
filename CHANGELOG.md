# Changelog

Binary downloads are available in [Releases](https://github.com/ByteRich/RichPaint/releases).

## 1.2.1 — 30 October 2026

### Windows and file opening

- Open one or more images from command-line paths, including filenames with spaces or Unicode characters.
- Offer Paintbro under Windows **Open with** for PNG, WebP, JPG/JPEG, GIF, and BMP after installation, preserving existing default applications.
- Support MSIX packaging for Microsoft Store distribution, including file associations.
- Paste an image from the clipboard into the empty workspace to open a new document with its original dimensions and transparency.

### Color picking and selection

- Pick colors anywhere on the screen with the native Windows pipette. Click to activate it, click to pick a color, or press Escape to cancel; holding the mouse button is unnecessary.
- Keep the pipette active until selection or cancellation and preserve the current color's opacity.
- Select the entire canvas with **Ctrl+A**, using a rectangle without rounded corners or feathered edges. Text inputs retain their normal select-all behavior.

### Workspace fixes

- Switch compact titlebar menus instantly without overlapping flyouts.
- Keep advanced color pickers inside the visible window, with scrolling when necessary.
- Disable elastic overscroll to prevent the entire application from shifting during laptop scrolling gestures.

## 1.1.0 — 29 October 2026

### Settings and keyboard shortcuts

- Save preferences automatically to `settings.json` and keyboard shortcuts separately to `keybinding.json`.
- Portable copies store both files in `paintbro-saved` beside `paintbro.exe`, so preferences can move with the application.
- Installed copies store both files in `%USERPROFILE%/Paintbro`.
- Migrate existing localStorage preferences and bindings from the older combined settings file automatically. An existing `keybinding.json` takes precedence.
- Save files atomically and flush pending changes before closing the application.

## 1.0 — 29 October 2026

Initial release of ByteRich Paintbro (version 1.0.0).

### Painting and image editing

- Paint with adjustable brushes, erase, fill areas, clone parts of an image, smudge colors, and lighten or darken pixels.
- Work with layers, groups, opacity, and layer masks.
- Add editable text, shapes, lines, curves, and arcs.
- Select areas with rectangle, ellipse, freehand, polygon, and magic-wand tools.
- Move, scale, and rotate layers; crop the canvas; use mirror painting and drawing guides.
- Adjust colors and apply filters with a preview before committing.

### Workspace and input

- Start from a new document, an existing image, or an image dropped into the app.
- Search commands and settings, customize supported keyboard shortcuts, and import or export your preferences and keybindings.
- Arrange dock panels, customize the toolbar and tool wheel, and save workspace layout presets.
- Palette with favorite and recent colors.

### Animation, export, and distribution

- Create and preview animations with editable frame timing and looping.
- Save images as PNG, JPEG, WebP, GIF, or BMP; export animations as GIFs.
- Use format-specific save options and reusable export presets.
- Get Paintbro as a Windows installer or an installer-free ZIP.

See [Capabilities](FEATURES.md) for more detail and [Saving and file formats](FAQ.md#how-does-saving-work) for what image exports preserve.

[Join the community](https://discord.gg/8pPUfE2Yv) · [Share feedback or report a bug](https://discord.gg/d8ChvYV9z)
