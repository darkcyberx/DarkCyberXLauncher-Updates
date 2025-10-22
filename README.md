# DarkCyberX Launcher Updates

This is the public update repository for the DarkCyberX GameLoop Launcher application.

## Repository Structure

```
DarkCyberXLauncher-Updates/
├── releases/
│   ├── v1.0.0/
│   │   ├── version.json
│   │   └── changelog.md
│   └── v1.1.0/
│       ├── version.json
│       └── changelog.md
├── latest.json
└── README.md
```

## How It Works

The DarkCyberX Launcher application checks this repository for updates by:

1. Reading the `latest.json` file to determine the latest available version
2. Comparing the latest version with the current application version
3. If an update is available, downloading the new executable from the specified download URL
4. Verifying the downloaded file using SHA256 hash and file size checks
5. Installing the update by replacing the current executable

## Adding New Releases

To add a new release:

1. Create a new folder in the `releases/` directory with the version number (e.g., `v1.2.0`)
2. Add the following files to the version folder:
   - `version.json` - Version information (see example format below)
   - `changelog.md` - Release notes and changes
3. Update `latest.json` to point to the new version and download URL

### version.json Format

```json
{
  "version": "1.2.0",
  "releaseDate": "2024-01-20",
  "downloadUrl": "https://example.com/downloads/DarkCyberXLauncher-v1.2.0.exe",
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
Executable files are hosted separately for better performance and to avoid GitHub's file size limitations.