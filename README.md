# DarkCyberX Launcher Updates

This is the public update repository for the DarkCyberX GameLoop Launcher application.

## Repository Structure

```
DarkCyberXLauncher-Updates/
├── releases/
│   ├── v1.0.0/
│   │   ├── DarkCyberXLauncher.exe
│   │   ├── version.json
│   │   └── changelog.md
│   └── v1.1.0/
│       ├── DarkCyberXLauncher.exe
│       ├── version.json
│       └── changelog.md
├── latest.json
└── README.md
```

## How It Works

The DarkCyberX Launcher application checks this repository for updates by:

1. Reading the `latest.json` file to determine the latest available version
2. Comparing the latest version with the current application version
3. If an update is available, downloading the new executable
4. Verifying the downloaded file using SHA256 hash and file size checks
5. Installing the update by replacing the current executable

## Adding New Releases

To add a new release:

1. Create a new folder in the `releases/` directory with the version number (e.g., `v1.2.0`)
2. Add the following files to the version folder:
   - `DarkCyberXLauncher.exe` - The new executable
   - `version.json` - Version information (see example format below)
   - `changelog.md` - Release notes and changes
3. Update `latest.json` to point to the new version

### version.json Format

```json
{
  "version": "1.2.0",
  "releaseDate": "2024-01-20",
  "downloadUrl": "https://github.com/DarkCyberX/DarkCyberXLauncher-Updates/releases/download/v1.2.0/DarkCyberXLauncher.exe",
  "changelogUrl": "https://raw.githubusercontent.com/DarkCyberX/DarkCyberXLauncher-Updates/main/releases/v1.2.0/changelog.md",
  "minimumVersion": "1.0.0",
  "critical": false
}
```

## Security

All updates are verified using:
- SHA256 hash verification
- File size verification
- Secure HTTPS downloads

## Notes

This repository is public and accessible to all users of the DarkCyberX GameLoop Launcher application.