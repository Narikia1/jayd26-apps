# JayD26 downloads

JayD26 saves video and audio from the web and converts video, audio and other files on your own device.
It is made by Narikia.

**Get it at [jayd26.narikia.com](https://jayd26.narikia.com).** The website always links to the latest release here.

| Device                   | File                                                                                    |
| ------------------------ | --------------------------------------------------------------------------------------- |
| Mac (macOS 14 or later)  | `JayD26-mac.dmg`, signed with an Apple Developer ID and notarized by Apple              |
| Windows 10 or 11, 64-bit | `JayD26-Setup.exe`, installs for you alone, with no administrator prompt                |
| Linux, 64-bit (x86-64)   | `JayD26-linux-x64.tar.gz`: unpack it, open the folder in a terminal, run `./install.sh` |
| Android 8 or later       | `JayD26-android.apk`                                                                    |
| iPhone and iPad          | Coming to the App Store                                                                 |

`SHA256SUMS.txt` in each release lets you check a download is the file we published:
`shasum -a 256 -c SHA256SUMS.txt` on Mac, `sha256sum -c --ignore-missing SHA256SUMS.txt` on Linux, or
`Get-FileHash JayD26-Setup.exe` on Windows.

## Open source inside

On Mac, Windows and Linux, JayD26 downloads with [yt-dlp](https://github.com/yt-dlp/yt-dlp) and converts with
[FFmpeg](https://ffmpeg.org), helped by [Deno](https://deno.com) and, on Windows, [aria2](https://aria2.github.io).
They are not part of the installer: the first time JayD26 runs, it fetches each one from its official release,
checks it against a published SHA-256, and refuses anything that does not match. Each keeps its own licence.
Questions: it@narikia.com.

## What is in this repository

Only the release workflow and the published files. The workflow builds and tests JayD26 on a real Windows
machine and a real Linux machine, installs it as people do, proves it starts, downloads and verifies the
engines, converts files, and keeps the installer, the Linux package and their test evidence as artifacts. It
publishes nothing by itself.
