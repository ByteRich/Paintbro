# Frequently asked questions

## Is Paintbro free?

Yes. ByteRich Paintbro is free to use.

## Who is it for?

Paintbro supports sketching, raster image editing, text and shape composition, and GIF animation. The interface emphasizes clear controls and visual consistency for new users, with command search, configurable shortcuts, and workspace presets for more customized workflows.

## Where do I download it?

Open [Releases](https://github.com/ByteRich/RichPaint/releases) and expand the **Assets** section of the release you want. Choose the Windows installer or portable ZIP for your PC. The release notes list available packages and any release-specific requirements.

GitHub also adds “Source code” archives automatically. Those contain this information repository; they aren't the Paintbro application.

## Can I open images from Windows Explorer or the command line?

Yes. Installer and Microsoft Store packages register Paintbro under **Open with** for `.png`, `.webp`, `.jpg`, `.jpeg`, `.gif`, and `.bmp`. Existing default image applications stay unchanged. Windows decides which apps appear directly in the submenu; look under **Choose another app** if Paintbro is not shown there.

Portable copies do not register themselves automatically. Use **Choose another app** to browse to the extracted `paintbro.exe`, or run the executable with one or more quoted image paths. Each external launch starts its own application instance. [Command-line example](GETTING-STARTED.md#2-create-or-open-a-document).

With no document open, you can also press `Ctrl+V` to open an image from the clipboard as a new document.

## Which platforms are available?

The packages documented here are for Windows. Use the release's architecture label to pick the right package: x64 for most Intel/AMD PCs, or ARM64 for Windows on ARM when that package is offered. macOS and Linux downloads aren't part of this release.

## What is WebView2, and do I need it?

Microsoft Edge WebView2 Runtime is a component Paintbro uses to display its interface. The installer can install it if it's missing. If the portable app reports that WebView2 is missing, use the Paintbro installer to set it up.

## Is the portable version fully self-contained?

It doesn't require a Paintbro installation. Extract the full ZIP and run `paintbro.exe`; WebView2 must already be present.

Portable settings are saved to `paintbro-saved/settings.json` beside `paintbro.exe`, with keyboard shortcuts in `paintbro-saved/keybinding.json`. Keep the included `paintbro-portable` marker beside the executable, and move the settings folder with the application to carry your preferences, shortcuts, palettes, layouts, and presets. The folder must be writable. Recent-file information and other WebView2 data still live in your Windows user profile.

## Where are settings saved?

Installed copies save settings to `%USERPROFILE%/Paintbro/settings.json`, for example `C:/Users/YourName/Paintbro/settings.json`. Portable copies use `<executable directory>/paintbro-saved/settings.json`. Keyboard shortcuts are stored separately in `keybinding.json` in the same directory as `settings.json`. Changes save automatically. Existing desktop preferences are migrated from the previous local storage when the settings file is first created. Bindings in an older combined settings file are moved into `keybinding.json`; an existing separate profile takes precedence.

You can also export preferences and keybindings separately from their settings screens.

## How does saving work?

Use **Save** (`Ctrl+S`) or **Save as** (`Ctrl+Shift+S`), then choose the format-specific options. Static image formats are PNG, JPEG, WebP, GIF, and BMP. Animated output uses GIF; you can also save a single frame as an image.

**There is no editable project-file format in this release.** Saving writes the rendered image or animation. Reopening that file won't restore separate layers, groups, masks, editable text and shapes, drawing guides, or undo history. Save different versions when you'd like to keep earlier results, and finish edits that need those objects before closing the document.

PNG is useful for transparency. JPEG uses a background color for transparent areas. GIF has a limited color palette and simple transparency, so it may look different from the canvas. Saving one frame doesn't save the rest of an animation.

Image exports use 8-bit color channels. Source metadata and embedded ICC color profiles aren't retained. If you need a workflow that preserves those, keep your original files.

## Can I change every shortcut?

You can customize supported commands in **Keybindings**, including adding alternative bindings and importing or exporting a profile. Some held keys, local controls, and mouse gestures aren't editable yet. [Keyboard and workspace tips →](KEYBOARD-AND-WORKSPACE.md)

## Where is the source code?

This repository contains product information and binary releases. The application's source code isn't published here.

## How do I report a bug or suggest something?

Use [Share feedback](https://discord.gg/d8ChvYV9z), the same destination linked from Paintbro's welcome screen. For a bug, include your Paintbro version, Windows version, the steps you took, what you expected, and what happened. A screenshot or small example image helps when you're comfortable sharing one.

For artwork, questions, and general chat, [join the community](https://discord.gg/8pPUfE2Yv). You can also find us on the [Paintbro website](https://www.byterich.org/paintbro) or explore [other ByteRich apps](https://www.byterich.org).

[Getting started](GETTING-STARTED.md) · [Changelog](CHANGELOG.md) · [Back to the README](README.md)
