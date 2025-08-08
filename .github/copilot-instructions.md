# Copilot Instructions for Resume-LaTeX

## Project Overview
This repository contains a LaTeX-based resume template, customized for iOS Developer roles. The main file is `resume.tex`, with modular sections in `sections/` and custom fonts in `fonts/`. The build process produces `resume.pdf`, which is then copied as `Takasur-Azeem-Resume-iOS-Developer.pdf` for distribution.

## Key Files & Structure
- `resume.tex`: Main LaTeX source file, includes sections from `sections/`
- `sections/`: Contains modular resume sections (e.g., `skills.tex`, `experience.tex`, etc.)
- `fonts/`: Custom Spectral font files used in the template
- `TLCresume.sty`: Custom style file for formatting
- `output/`: (if present) for build artifacts

## Build Workflow
To build and export the resume PDF, run:

```sh
lualatex resume.tex && cp resume.pdf ../Takasur-Azeem-Resume-iOS-Developer.pdf
```
- Run this command from the repository root.
- Requires `lualatex` (from TeX Live).
- Fonts must be present in `fonts/`.

## Editing & Customization
- Add or update resume sections in `sections/`.
- For experience entries, use `sections/experiences/`.
- Update `resume.tex` to include or reorder sections as needed.
- Style changes go in `TLCresume.sty`.

## Conventions & Patterns
- Section files are modular for easy editing and reuse.
- Font files are referenced directly for consistent rendering.
- Output PDF is always copied to the parent directory for easy access.

## Integration Points
- No external APIs or services; all dependencies are local (LaTeX, fonts).
- No automated tests; manual build and inspection required.

## Example: Adding a New Experience
1. Create a new file in `sections/experiences/` (e.g., `12-new-company.tex`).
2. Reference it in `sections/experience.tex`.
3. Rebuild using the workflow above.

For questions or unclear conventions, review `README.md` or ask for clarification.

## How to Build Resume

To compile the LaTeX resume and copy the output PDF for iOS Developer:

```sh
lualatex resume.tex && cp resume.pdf ../Takasur-Azeem-Resume-iOS-Developer.pdf
```


## Recommended Usage


[IMPORTANT: Commit Message Convention]
End each commit message with الحمدالله


For automation, add this command to your CI/CD or build scripts as needed.
