EmuDrop — RG DS Plus ROCKNIX Controller Fix

An unofficial ARM64 compatibility patch for "EmuDrop" (https://github.com/ahmadteeb/EmuDrop) on the Anbernic RG DS Plus running ROCKNIX.

Download

"Download the latest release" (https://github.com/disgro/EmuDrop-RGDSPlus/releases/latest)

This release fixes controller navigation without requiring users to rebuild EmuDrop.

What's Fixed

- D-pad: Up, Down, Left, Right
- Left analog stick: Directional navigation
- ROCKNIX controller compatibility where the D-pad is reported as joystick buttons rather than hat inputs

Tested Hardware

Component| Configuration
Device| Anbernic RG DS Plus
Operating System| ROCKNIX 20261001
Processor| RK3566
Architecture| ARM64 / AArch64
Status| Working — tested on physical hardware

Other devices and ROCKNIX versions have not been verified.

Installation

Requires an existing EmuDrop installation.

1. Download the ARM64 ZIP from the latest release.

2. Extract the "EmuDrop" executable.

3. Connect to your device using a file manager or SSH.

4. Navigate to "/storage/roms/ports/EmuDropKnulli/".

5. Rename the original "EmuDrop" executable to "EmuDrop_old".

6. Copy the patched "EmuDrop" executable into that directory.

7. Set executable permissions using SSH:
   
   chmod +x /storage/roms/ports/EmuDropKnulli/EmuDrop

8. Ensure the existing "EmuDrop.sh" launcher exports "PYSDL2_DLL_PATH=/usr/lib".

9. Launch EmuDrop through the ROCKNIX Ports menu.

Important: Keep the original "assets" directory and back up your existing launcher before making changes.

Building from Source

The repository includes:

- "navigation.patch" — controller compatibility changes
- ".github/workflows/build.yml" — GitHub Actions ARM64 build workflow

Run Build EmuDrop ARM64 from the Actions tab to compile a new executable.

Credits

Original EmuDrop developed by "ahmadteeb" (https://github.com/ahmadteeb/EmuDrop).

This repository provides an unofficial community compatibility modification. It is not affiliated with or endorsed by the original developer.

Feedback

Found a bug or tested another device? "Open an issue" (https://github.com/disgro/EmuDrop-RGDSPlus/issues) with your device model, ROCKNIX version, and results.
