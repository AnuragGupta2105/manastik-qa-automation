# Manastik Medico — QA Automation

## Project Overview
This repository contains manual test cases and UI automation tests for the Manastik Medico Android application, using Maestro.

## Test Environment
- Platform: Android Emulator
- Application package: `com.manastik.dadtmedico`
- Automation framework: Maestro 2.11.0
- Java: JDK 21
- Operating system: Windows

## Project Structure
- `test-cases/` — Manual test cases
- `tests/maestro/` — Maestro automation flows and UI hierarchy
- `evidence/` — Screenshots and supporting evidence
- `bug-reports/` — Bug reports and investigation notes
- `test-results.txt` — Recorded automation results

## Prerequisites
1. Install Android Studio and create/start an Android emulator.
2. Install the supplied Manastik Medico APK on the emulator.
3. Install Java and Maestro CLI.
4. Ensure ADB can detect the emulator.

Check the connected device:
```powershell
adb devices
```

Check Maestro:
```powershell
maestro --version
```

## Running the Tests
Run the verification screen test:
```powershell
maestro test "tests/maestro/verification-pending.yaml"
```

Run the app-launch smoke test:
```powershell
maestro test "tests/maestro/app-launch.yaml"
```

Validate a flow's syntax:
```powershell
maestro check-syntax "tests/maestro/app-launch.yaml"
```

Run these commands from the repository root. If needed, replace the relative paths with full Windows paths.

## Current Automation Coverage
The current flows launch the app and check that the "Verification in progress" heading is visible. Both flows cover the same screen and are not independent functional tests.

## Known Limitations
- The current automation coverage is limited to the verification-pending screen.
- Negative onboarding scenarios and other screens still need additional automated coverage.
- A passing test confirms only the assertions in that flow; it does not confirm that the entire onboarding process works.
- Only report bugs that have been reproduced and supported by evidence.

## Results
See `test-results.txt` for recorded runs. Results may depend on the app's saved state and emulator state.

## Submission Checklist
- [ ] Review manual test cases
- [ ] Add actionable bug reports where reproducible issues are found
- [ ] Verify evidence matches the reported tests
- [ ] Record a short demonstration video
- [ ] Push the repository to GitHub
- [ ] Share the deliverables folder and repository link

## Privacy
Do not include private credentials, OTPs, personal information, or any hiring-team answer key in the public repository.
