# DG-Apps-Essential-v1.2.0
DG App Collection
DG App Collection - Portable App Launcher v1.1.0
=================================================

What this is
------------
A portable collection of DG tools and utilities with a single launcher.
No installation is required. Windows 10/11 with the built-in PowerShell 5.1.

How to start the launcher
-------------------------
Option 1 (recommended, portable): double-click  Launch.cmd
Option 2: double-click  _Launcher\AppLauncher.cmd
Option 3: double-click  App Launcher.lnk  (works while the folder is at
          C:\Users\DG\Desktop\DG-App-Collection)

Note: .ps1 files are not associated with PowerShell on every PC, so use
one of the .cmd / .lnk entries above instead of opening AppLauncher.ps1.

Using the launcher
------------------
- Search: type in the search box to filter by app name or path.
- Category: choose All / GUI / Console / Installers / etc.
- Show installers: tick to include setup/installer entries.
- Launch: select an app and click "Launch app", or double-click it.
- Install app: runs the selected installer elevated (UAC prompt).
- Open folder: opens the folder that contains the selected app.
- Refresh: rescans the Apps folder after adding or removing files.
- The header shows the launcher version (v1.1.0).

What is included
----------------
- Apps\                  Portable apps and installers (the launcher scans this folder).
- DG Command Center\     DG Command Center 2.5.0 (full application).
- _Launcher\             Launcher scripts and icon.
- Launch.cmd             Portable launcher entry point.
- App Launcher.lnk       Desktop shortcut (absolute path; use Launch.cmd if moved).

Adding your own apps
--------------------
Copy any .exe, .cmd, .bat, .ps1, .lnk or .msi into Apps\ (subfolders are fine),
then click Refresh in the launcher.

Troubleshooting
---------------
- Nothing happens: right-click Launch.cmd -> Run, or run
  powershell.exe -NoProfile -ExecutionPolicy Bypass -File "_Launcher\AppLauncher.ps1"
- Check _Launcher\launcher.log and _Launcher\launcher-error.log for details.
- If PowerShell is blocked by policy, use the .cmd files (they pass
  -ExecutionPolicy Bypass for this process only).
- Some apps require administrator rights; use "Install app" or run the
  launcher as administrator.

Version history
---------------
v1.1.0 - Fixed filter/launch event handlers (closure scoping), added version
         badge and startup logging, cleaned duplicate files from the package.
