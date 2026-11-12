# Security Policy

## Supported versions

Only the latest release is supported.

## Reporting a vulnerability

Please report security issues privately through GitHub:
[Report a vulnerability](https://github.com/croustibat/memo2mp3/security/advisories/new).
Do not open a public issue for a security problem.

You can expect a first answer within a week.

## Scope

`memo2mp3` is a single bash script. It reads the Voice Memos library in
read-only mode, runs `ffmpeg` locally and writes an MP3. It makes no network
requests and never modifies your recordings.
