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
