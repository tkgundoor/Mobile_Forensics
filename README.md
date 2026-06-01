# Mobile Forensic Toolkit

A starter mobile forensic toolkit for Android and Apple devices.

## Features

- Android device collection via `adb`
- Android backup analysis for contacts, SMS, and call logs
- Apple backup analysis using iTunes/MobileSync backups
- Report generation for collected artifacts

## Requirements

- Python 3.9+
- `adb` available on PATH for Android collection
- Access to Apple backup directory for iOS analysis

## Installation

```powershell
cd Mobile_Forensic
python -m pip install -r requirements.txt
```

## Usage

Run the CLI via:

```powershell
python -m forensic_toolkit.cli --help
```

### Android

List connected devices:

```powershell
python -m forensic_toolkit.cli android-list
```

Collect device information:

```powershell
python -m forensic_toolkit.cli android-collect --output reports/android
```
```

Analyze an Android backup folder:

```powershell
python -m forensic_toolkit.cli android-analyze --backup-dir path\to\android_backup --output reports/android
```

### Apple

Analyze an Apple backup folder:

```powershell
python -m forensic_toolkit.cli apple-analyze --backup-dir path\to\apple_backup --output reports/apple
```

## Notes

This project is a foundation. Extend the toolkit by adding more artifact parsers, file extraction, timeline generation, and forensic reporting.
