# Blue Screen Troubleshooting

## Issue
User reports Blue Screen error when starting Windows.

## Initial Checks
- Asked user what error code appears.
- Confirmed if new hardware or software was installed.
- Checked if issue happens every boot.

## Troubleshooting Steps
1. Booted into Safe Mode.
2. Ran `sfc /scannow`.
3. Checked Event Viewer logs.
4. Updated drivers.
5. Checked RAM using Windows Memory Diagnostic.

## Resolution
Outdated network driver was causing system crash.
Updated driver → system stable.

## Prevention
Keep drivers updated and avoid installing unsigned software.
