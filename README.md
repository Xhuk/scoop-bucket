# scoop-bucket

Scoop manifests for Xhuk projects.

## Install edgePass

```powershell
scoop bucket add xhuk https://github.com/Xhuk/scoop-bucket
scoop install edgepass
```

## Requirements

OpenBao 2.x is a prerequisite. Install it, initialize it, and unseal it before you
start edgePass. See the project README:

https://github.com/Xhuk/EdgePass

## Notes

- The manifest installs the portable executable, not the NSIS installer.
- The binary is self-signed, so SmartScreen may warn about the publisher.
- Scoop does not apply the downloaded-file mark, so the install does not go through
  the SmartScreen prompt.

## Update

```powershell
scoop update
scoop update edgepass
```
