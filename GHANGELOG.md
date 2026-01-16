# Changelog

All notable changes to GrokDevPrompt will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.3] - 2026-01-15

### Added / Improved

- **Self-improvement loop refinements** (major focus of this version)
  - The generated meta-prompt now correctly references the live tool URL:  
    `https://medicinalsheep.github.io/grokdevprompt/`
  - No longer calls the output "GrokDevPrompt vX.X" — instead produces a "Project-Specific Prompt Generator – Iteration #X – [project-type]-Specialized"
  - Tracks and displays **self-improvement loop iteration number** (starts at #1, Grok should increment in subsequent generations)
  - When fields are empty, now shows **"not yet specified"** instead of "none" for:  
    Common Features, Custom Features, Tech/Stack, Non-functional Requirements, Additional Instructions
  - When **Truncate or multiple response** is selected:  
    → Removes the final "Do not truncate." sentence from the generated prompt  
    → Keeps only the proper truncation instructions (`// TRUNCATED HERE` + "Reply 'ready' to continue...")

### Fixed

- Cleaner, more consistent wording in the self-improvement meta-prompt
- Better separation between tool identity and project-specific specialization

### Notes

v0.3 is the first version where the self-improvement loop feels significantly more polished and self-aware —  
the rabbit hole is now officially signposted with mile markers. 🌀

Next iterations should get even more context-aware and project-tailored.

## [0.2] - 2026-01-14

### Added

- **Desired visual theme / style input field**  
  New optional textarea: "Desired visual theme / style / color scheme for the final product"  
  Appears only in self-improved versions of the tool (after using the self-improvement loop)  
  Includes smart tooltip with examples (cyberpunk, minimalist light, retro 8-bit, corporate blue, etc.)  
  Prevents forcing the GrokDevPrompt dark cyberpunk aesthetic onto generated projects unless explicitly wanted

- **Smarter theme detection**  
  The self-improvement prompt now checks existing inputs (description, tech stack, requirements, additional instructions) for theme-related keywords  
  If detected, suggests pre-filling the new theme field with a best-guess value

- **Better self-evolution targeting**  
  Generated prompts now explicitly include the desired final product theme in the output prompt template  
  Falls back gracefully to "modern, clean, professional default appropriate for [project type]" when left blank

### Improved

- Self-improvement loop logic made more robust and context-aware  
  Better preservation of original prompt structure while layering in project-specific intelligence  
  Clearer instructions to Grok about maintaining the tool's signature dark cyberpunk UI while decoupling it from the final product output

### Fixed / Refined

- More precise wording in the meta-prompt to avoid accidental theme bleed into generated projects
- Enhanced guidance in tooltips for the new theme field to help users understand its purpose and power

### Notes

This version marks the first meaningful evolution produced via the self-improvement loop itself —  
a nice little meta milestone for the tool's design philosophy.

Happy rabbit-hole diving! 🌀
## [0.1] - 2026-01-14

### Added

- Initial public release
- Beautiful dark cyberpunk UI
- 15+ project types including:
  - Unity Game
  - Unreal Engine Project
  - VR/AR App
  - AI/ML Tool
  - Blockchain App
  - Game Mod
  - Steam Integrated App
- 25+ common feature checkboxes:
  - High-resolution graphics (4K/retina)
  - AI integration
  - VR/AR support
  - Procedural generation
  - Modding support
  - Steamworks integration
  - Monetization, cloud sync, analytics, physics engine, i18n...
- Experimental features section:
  - "Truncate or multiple response" mode
  - "Prompt self-improvement loop" (meta-prompt that evolves the tool)
- Tooltip help system
- Responsive design
- Copy to clipboard functionality

### Changed

- Project structure cleaned up for GitHub publication
- Version bumped to 0.1 for first public release

## [0.0] - 2026-01 (pre-release)

- Internal testing/initial release
- Basic project basics, features, tech stack inputs
- Simple prompt generation
