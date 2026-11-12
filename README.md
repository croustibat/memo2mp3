# memo2mp3

Convert an Apple Voice Memos recording to MP3, in one command.

Recent versions of Voice Memos save recordings as `.qta` files with a spatial audio track. Slack, Discord, WhatsApp and most players can't read them, and the app has no "export as MP3". `memo2mp3` reads the Voice Memos library on your Mac, picks a recording and writes a plain stereo MP3 named after its title.

## Install

```sh
brew install croustibat/tap/memo2mp3
```

Or copy the `memo2mp3` script anywhere on your `PATH` (requires `ffmpeg`).

## Usage

```sh
memo2mp3              # convert the latest recording
memo2mp3 3            # convert the 3rd most recent
memo2mp3 2026-10-13   # convert the last recording of that day
memo2mp3 -l           # list the 15 most recent recordings
```

The command prints the path of the MP3. Files go to `~/Music/memo2mp3`; set `MEMO2MP3_DIR` to change that.

## Requirements

- macOS with Voice Memos (recordings made on an iPhone show up once iCloud has synced them).
- **Full Disk Access** for your terminal app (System Settings > Privacy & Security > Full Disk Access). Without it macOS blocks access to the Voice Memos library.

## Caveats

- `memo2mp3` reads Voice Memos' internal database (`CloudRecordings.db`), which Apple does not document. A macOS update can break it. It only ever reads; it never modifies your recordings.
- A recording that is still in iCloud only has to be opened once in Voice Memos before it can be converted.

## License

MIT
