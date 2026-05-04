# Codex Pet Runs

**Part of my AI-Assisted Learning Journey** | [View Full Series](#more-in-this-series)

> A fun Codex project for generating tiny animated pets.
> This first run features Cupcake, a soft cream-and-gray cat with big blue eyes.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](/LICENSE)

---

## Learning Focus

- AI-assisted visual asset generation
- Prompting Codex for creative project workflows
- Sprite atlas structure and validation
- Small, shareable GitHub projects with generated assets

---

## What Is This?

This repository is a playful pet-generation run made with Codex. It is not a public store package or production asset pipeline. It is simply a place to share Cupcake and the project structure behind the generated sprite pet.

If you like Cupcake, feel free to fork this repo, keep the cat, remix the prompts, or ask your own Codex session to generate a new pet for you.

---

## Featured Pet

### Cupcake

Cupcake is a tiny cream-and-gray cat with tabby face stripes, white paws, big round blue eyes, and a curious expression.

The final sprite atlas lives at:

```text
cupcake/final/spritesheet.webp
```

The generated pet includes animation rows for idle, running, waving, jumping, failed, waiting, and review states.

---

## Project Structure

```text
cupcake/
├── pet_request.json        # Pet metadata, atlas dimensions, row layout
├── prompts/                # Base and row-specific generation prompts
├── frames/                 # Per-state generated animation frames
├── qa/                     # Review summaries and QA artifacts
└── final/
    ├── spritesheet.webp    # Final Cupcake sprite atlas
    └── validation.json     # Validation result for the atlas

cupcake-input/
└── cupcake-reference.png   # Original reference image
```

---

## Use It However You Like

This is here for fun sharing. You can:

- Fork it and keep Cupcake in your own collection
- Use the structure as inspiration for your own Codex pet run
- Replace the reference image and ask Codex to generate a new character
- Browse the prompts to see how the pet states were described

No formal reproduction steps are included because the point is exploration, remixing, and giving Codex a cute creative target.

---

## Make Your Own Pet

Want a pet like Cupcake? Open Codex Desktop and ask Codex to help you hatch one.

1. Open Codex Desktop.
2. Make sure the built-in skill installer is available. In current Codex, `skill-installer` is a system skill, so you usually do not need to install it separately.
3. Install the curated Hatch Pet skill:

```text
$skill-installer hatch-pet
```

4. Restart Codex so the new skill is loaded.
5. Invoke the installed skill directly and describe the companion you want, or upload a reference picture:

```text
$hatch-pet create a tiny pixel-style corgi with a blue scarf.
```

Natural language also works, for example: `Use hatch-pet to create a pet from this reference image.`

The fun part is the prompt. Give Codex a personality, colors, accessories, or a photo, then let it turn the idea into a Codex-compatible animated pet package.

---

## About This Learning Journey

### My Approach

This project is part of my AI-assisted learning methodology:

1. **ChatGPT for Brainstorming** - Initial ideation and project scoping
2. **Gemini / Google AI Studio for UI** - Quick setup and visual exploration
3. **Hands-on Building** - Claude Code, Codex, and GitHub Copilot for real project work
4. **Research Support** - Gemini Deep Research and Claude for tutorials, documentation, and writing

### More in This Series

1. **[Private] Real-world local shop website quick setup** - Prompt Engineering ✅
2. **[Brainstormed Claude Skills Archive](https://github.com/HaominHU/claude-code-skills-archive)** - Prompt Engineering + Claude Skills Creation ✅
3. **[Caregiver Agent Prototype](https://github.com/HaominHU/mvp-cg-agent)** - Agent Architecture & Orchestration ✅
4. **[This Project] Codex Pet Runs** - Codex Creative Asset Generation ✅


---

## License & Acknowledgments

**License:** MIT

**AI Tools Used:**

- Codex - Pet generation workflow, sprite validation, and repository documentation
- ChatGPT - Brainstorming and writing support

---

*Part of the AI-Assisted Learning Journey series | Last updated: May 2026*
