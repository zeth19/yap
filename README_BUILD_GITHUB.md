# LOUI EXT — GitHub Actions build

1. Create a **private** GitHub repository.
2. Upload the *contents* of the LOUI-EXT source directory to the repository root (not an extra nested LOUI-EXT folder).
3. Ensure `.github/workflows/build.yml` is included (GitHub web upload may hide dotfolders; create it via Add file > Create new file with path `.github/workflows/build.yml` if needed).
4. Open Actions > Build LOUI EXT (Android ARM64) > Run workflow.
5. Wait for the build to finish. Download the artifact `LOUI-EXT-arm64-v8a` from the workflow run.

The project uses Android.mk / Application.mk and builds an Android ARM64 native executable (`Starcool.sh`), not an APK. NDK r27c (27.2.12479018) is installed on an Ubuntu 24.04 runner. If the build fails, inspect the first compiler/linker error in the build log; success is not guaranteed without testing.

Do not upload credentials, personal data, or secrets into the repository.
