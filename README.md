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

The Microsoft Edge **WebView2 Runtime** is also required. Windows 11 ships it;
Windows 10 needs the Evergreen Runtime:
https://developer.microsoft.com/microsoft-edge/webview2/

## Notes

- The manifest installs the portable executable, not the NSIS installer.
- The binary is self-signed, so SmartScreen may warn about the publisher.
- Scoop does not apply the downloaded-file mark, so the install does not go through
  the SmartScreen prompt.
- **Quit edgePass before `scoop update edgepass`.** Windows cannot replace a
  running `.exe`; with the widget open the old version cannot be removed.
- Config, index and logs live in `%APPDATA%\edgePass` and
  `%LOCALAPPDATA%\edgePass`, not inside the Scoop directory, so `scoop update`
  never touches them and uninstalling does not delete them. Remove those folders
  yourself if you want a clean slate.
- `scoop uninstall edgepass` also removes the `edgePass` logon task, if it was
  enabled from Ajustes.

## Update

```powershell
scoop update
scoop update edgepass
```
