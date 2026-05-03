name: Mod Request
description: Suggest a new mod for the BadPCMC performance pack (Modrinth only)
title: "[Mod Request] <Mod Name>"
labels: ["enhancement", "mod request"]
assignees: []

body:
  - type: input
    id: mod_name
    attributes:
      label: Mod Name
      description: Exact name of the mod you are suggesting.
      placeholder: e.g., Sodium
    validations:
      required: true

  - type: input
    id: modrinth_link
    attributes:
      label: Modrinth Link
      description: Only Modrinth links are accepted. Paste the full URL to the mod’s Modrinth page.
      placeholder: https://modrinth.com/mod/sodium
    validations:
      required: true

  - type: dropdown
    id: mod_category
    attributes:
      label: Mod Category
      description: What kind of mod is this?
      options:
        - Performance
        - Bug Fix
        - Quality of Life
        - Library
        - Other
    validations:
      required: true

  - type: dropdown
    id: mod_loader
    attributes:
      label: Mod Loader
      description: Which mod loader does it support? Must be compatible with the pack’s loader.
      options:
        - Fabric
        - Forge
        - NeoForge
        - Quilt
    validations:
      required: true

  - type: input
    id: mc_versions
    attributes:
      label: Supported Minecraft Version(s)
      description: e.g., 1.20.1, 1.21
      placeholder: 1.20.1
    validations:
      required: true

  - type: textarea
    id: reason
    attributes:
      label: Why should this be added?
      description: Explain how this mod improves performance, fixes an issue, or fills a gap that the current BadPCMC pack doesn’t cover.
    validations:
      required: true

  - type: dropdown
    id: compatibility_tested
    attributes:
      label: Have you tested it with BadPCMC?
      options:
        - "Yes"
        - "No"
        - "Not yet"
    validations:
      required: true

  - type: textarea
    id: known_conflicts
    attributes:
      label: Known Conflicts
      description: Any known conflicts with existing mods in the pack?
      placeholder: Leave empty if none.

  - type: textarea
    id: dependencies
    attributes:
      label: Dependencies
      description: Does it require additional libraries or other mods? List them with Modrinth links if possible.
      placeholder: e.g., Fabric API, Cloth Config

  - type: textarea
    id: additional_context
    attributes:
      label: Additional Context
      description: Benchmarks, comparisons, issue references, or anything else helpful.

  - type: checkboxes
    id: checklist
    attributes:
      label: Final Checks
      options:
        - label: I have verified this mod is **not already in** the BadPCMC pack.
          required: true
        - label: The mod is **actively maintained** and supports the pack’s Minecraft version.
          required: true
        - label: I understand only **Modrinth** sources will be considered.
          required: true
