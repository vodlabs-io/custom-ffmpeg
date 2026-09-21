# custom-ffmpeg

Minimal static FFmpeg binaries optimized for post-processing recorded live streams.

| Build Type | Size per Binary |
|------------|----------------|
| Full FFmpeg | 65-90 MB |
| Minimal Build | 8-15 MB |

## Supported Platforms

- macOS Intel (darwin_amd64)
- macOS Apple Silicon (darwin_arm64)  
- Linux x86_64 (linux_amd64)
- Linux ARM64 (linux_arm64)
- Windows x86_64 (windows_amd64)

## Creating a Release

To build new FFmpeg binaries:

1. Go to GitHub Actions tab
2. Select "Build Minimal FFmpeg" workflow  
3. Click "Run workflow"
4. Wait for builds to complete

Each build is pinned to an exact FFmpeg tag and x264 commit, set at the top of
`.github/workflows/build-ffmpeg.yml` (`FFMPEG_TAG`, `X264_COMMIT`). Bump them
deliberately, in a commit that names the new revisions.

## License

The binaries are **GPL-2.0-or-later**: they're built with `--enable-gpl
--enable-libx264`, and libx264 is itself GPL. Every release therefore
includes, alongside each `ffmpeg-<platform>.tar.gz`:

- `ffmpeg-<platform>-NOTICE.txt` — the exact `configure` invocation used for
  that platform, and where to get the source.
- `ffmpeg-x264-sources.tar.gz` — the complete, unmodified FFmpeg and x264
  source trees at the pinned revisions above, plus the workflow file that
  controls compilation. Attached once per release, shared by every platform.

This repository's own code (the build workflow, this README) is licensed
under the [MIT License](LICENSE) — a separate license from the binaries it
produces.
