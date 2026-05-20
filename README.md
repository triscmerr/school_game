# school_game
This project will grow into interactive classroom games and activities

## Running Word Wall

Serve the folder with any static web server and open `index.html` in a browser.
Opening `index.html` directly from the filesystem still works for manual
selection, but browsers may block automatic loading of neighboring files.

## Word Wall configuration

On startup, the game looks for `word-wall-config.json` in the same directory as
`index.html`. The configuration maps image filenames to audio filenames, and the
game then tries to load those image and audio files from that same directory.

If no configured image files are found, the game stays on the main menu. Use
`Browse Folder` to select the folder containing the configured media, or use the
separate image and audio pickers.

Example:

```json
{
  "items": [
    { "image": "1.png", "audio": "1.m4a" },
    { "image": "2.png", "audio": "2.m4a" },
    { "image": "3.png", "audio": "" }
  ]
}
```

Images that load successfully are used. Missing images are skipped. Missing audio
files are skipped and those tiles use the default sound. Use `Save Configuration
File` to download the current mapping as `word-wall-config.json`.
