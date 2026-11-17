# Teleprompter

A browser teleprompter with a Hebrew interface, support for Hebrew and Arabic scripts, and mirror modes for use with a beam splitter or an inverted display. The application is a single HTML file with no build step or external dependencies.

## Run locally

Open `index.html` in a browser, or run a local server from the repository directory for reliable browser storage:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Then open <http://127.0.0.1:8000/>. On a shared computer, use a private browser window for scripts you want to keep out of the browser profile.

## Use it

1. Open the editor from the toolbar, paste or type your script, and choose **שמירה והצגה**.
2. Set the font, text size, margins, colors, and scroll speed.
3. Start scrolling with the play button. Use horizontal or vertical mirroring if your display setup requires it.

| Key | Action |
| --- | --- |
| Space | Start or pause scrolling |
| Home | Return to the start |
| ↑ / ↓ | Scroll manually |
| + / − | Adjust text size |
| F | Toggle fullscreen when supported by the browser |
| Ctrl / ⌘ + Enter | Save and close the editor |

## Privacy

The app does not send your text to a server. It saves the script and display preferences in the browser's local storage for the current origin. Clear site data to remove them from that browser profile. Pasted text is displayed as plain text.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for local checks and guidance on reporting issues. The project uses the [MIT License](LICENSE).
