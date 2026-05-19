# school_game
This project will grow into interactive classroom games and activities

## Word Wall configuration

On startup, the app looks for `word-wall-config.json` next to `index.html`.
If the file is missing, empty, or has no usable image entries, the app starts in
the normal manual upload mode.
Configured files must be reachable by the browser, usually in the same folder as
`index.html` or through a relative path from that folder.

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
files are skipped and those tiles use the default sound.
