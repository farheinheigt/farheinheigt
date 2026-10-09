# Profile content, data, and updates

## Profile page

`README.md` is the public profile. It presents Farid's name and ethical-hacking focus with four generated SVGs: the repository galaxy, activity, languages, and featured projects. Each image adapts to light or dark appearance and narrow screens. `README.profile.md` mirrors the profile markup for the generator's checks.

The featured projects are CTFoutu, Rappel, and mesip. The links are LinkedIn and the existing TryHackMe badge. No email address is published by this profile.

## Data and automation

The generator reads public repository metadata for `farheinheigt`. `config.yml` groups repositories by security and CTFs, macOS and shell, and Rust CLI tools. It does not request private repository contents.

The GitHub Action generates real profile assets on pushes to the configuration or generator and every 12 hours. The generated SVGs are committed to `assets/generated/` so the profile does not depend on a runtime image service.

## Acceptance criteria

- `README.md` references all generated image variants with meaningful alternative text.
- Production generation uses `config.yml`, not the demo fixture.
- Every featured repository exists and belongs to the configured focus area.
- The README links resolve to files or public profile pages.
