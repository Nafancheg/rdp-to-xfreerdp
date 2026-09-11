# RDP to XFreeRDP

A small, dependency-free browser tool that converts Microsoft `.rdp` connection files into an `xfreerdp` command for Linux.

The converter runs entirely in the browser: the selected RDP file is not uploaded anywhere.

## Features

- Drag-and-drop `.rdp` files
- UTF-16 LE/BE and UTF-8 decoding
- Desktop sessions and RemoteApp
- RDS collection/load-balancing support via `loadbalanceinfo`
- Clipboard, printer and smart-card redirection
- Multi-monitor sessions
- Session color depth and non-default RDP ports
- Auto reconnect and dynamic resolution for desktop sessions
- Password prompt through Zenity
- One-click command copy

## Usage

1. Open `index.html` in a modern browser.
2. Drop an `.rdp` file onto the page or click the drop area.
3. Review the generated command.
4. Copy it and run it on the target Linux workstation.

The Linux workstation needs FreeRDP (`xfreerdp`) and Zenity installed.

## Notes

The project was originally made for a specific corporate environment, so several defaults are intentionally opinionated. Review the defaults in `buildXFreeRdpCommand()` before using it in another environment.

The generated command asks for the password interactively and does not read a saved password from the source RDP file.

## GitHub Pages

The project is a static single-page application, so `index.html` can be hosted directly with GitHub Pages from the repository root.

## License

MIT