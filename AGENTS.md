# Repository Guidelines

## Project Structure & Module Organization

This repository stores generated pet sprite assets and their supporting prompts. The current pet is under `cupcake/`.

- `cupcake/pet_request.json` defines the pet metadata, atlas size, row order, frame counts, and layout guide references.
- `cupcake/prompts/base-pet.md` and `cupcake/prompts/rows/*.md` hold generation prompts. Keep row prompt filenames aligned with state names such as `idle`, `running-right`, and `review`.
- `cupcake/frames/<state>/` contains per-state frame outputs.
- `cupcake/final/spritesheet.webp` is the assembled 8x9 atlas; `cupcake/final/validation.json` records validation results.
- `cupcake/qa/` contains review artifacts and run summaries.
- `cupcake-input/` contains source reference art, currently `cupcake-reference.png`.

## Build, Test, and Development Commands

There is no package manager or checked-in build script in this repository. Use local inspection and validation commands:

- `rg --files` lists tracked project files quickly.
- `jq . cupcake/pet_request.json` checks that the request manifest is valid JSON.
- `jq '.ok, .errors, .warnings' cupcake/final/validation.json` reviews the latest sprite validation result.
- `file cupcake/final/spritesheet.webp` confirms the exported atlas format.

When regenerating assets, keep outputs within the existing pet folder and update the manifest, prompts, frames, QA results, and final atlas together.

## Coding Style & Naming Conventions

Use two-space indentation for JSON. Keep Markdown prompts concise, with descriptive headings and state-specific instructions. Use lowercase kebab-case for animation states and paths, matching the existing pattern: `running-left`, `running-right`, `base-pet.md`. Do not rename states without updating `pet_request.json`, prompt files, frame directories, and validation expectations.

## Testing Guidelines

Before committing asset changes, verify that `cupcake/final/validation.json` has `"ok": true`, no errors, and expected transparent unused cells. Confirm atlas dimensions match `pet_request.json`: 1536x1872, 8 columns, 9 rows, 192x208 cells. Review `cupcake/qa/review.json` and any QA videos when animation timing or visual consistency changes.

## Commit & Pull Request Guidelines

Git history currently only contains the initial commit, so use clear, imperative commit messages such as `Update cupcake idle frames` or `Regenerate cupcake spritesheet`. Pull requests should describe which states changed, note whether prompts or source references changed, and include screenshots or QA previews for visual updates. Link related issues when available and call out any validation warnings that remain.

## Agent-Specific Instructions

Avoid unrelated asset churn. Generated binary files can be large, so change only the pet states required by the task and keep manifests synchronized with generated outputs.
