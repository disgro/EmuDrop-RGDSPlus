# EmuDrop RG DS Plus ARM64 build workflow (UNTESTED)

This workflow fetches upstream EmuDrop, checks/applies `navigation.patch`, builds an ARM64 Linux PyInstaller executable and uploads it as a GitHub Actions artifact.

## Important
- This is a build *recipe*, not a compiled application.
- It deliberately fails if the patch does not match the current upstream source. Do not bypass that check.
- The resulting executable has not been tested on ROCKNIX. ARM64 architecture alone does not guarantee library/GLIBC compatibility.
- Do not overwrite your existing working EmuDrop binary until a build has succeeded and the new executable has been tested separately.

## Usage
Place `.github/workflows/build-arm64.yml` and `navigation.patch` in a GitHub repository, enable Actions, then manually run **Build EmuDrop RG DS Plus ARM64**. Download the artifact if the build succeeds. Inspect the logs if it fails.
