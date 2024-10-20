# Town of Salem: Anticipation Roles Data

## Role Data Format

The roles data is stored in JSON format. They have the following properties:

- `faction`: List of factions:
  - `name`: Name of faction
  - `limit`: Maximum allowed occurence of faction in rolelist (`-1` if no limit)
  - `aliases`: List of possible aliases for faction
  - `require`: List of roles that are guaranteed a slot (Optional)
  - `require_min`: Minimum amount of roles of the factions in the list for requirement to take effect (Optional)
  - `fallback`: Entry to roll to meet requirement (Optional)
  - `alignments`: List of alignments in faction:
    - `name`: Name of alignment
    - `limit`: Maximum allowed occurence of alignment in rolelist (`-1` if no limit)
    - `aliases`: List of possible aliases for alignment
    - `roles`: List of roles in alignment:
      - `name`: Name of role
      - `ascii_name`: Alternative name of role for ASCII platforms (Optional)
      - `limit`: Maximum allowed occurence of role in rolelist (`-1` if no limit)
      - `aliases`: List of possible aliases for role
      - `wincon`: ID of win condition for role (`-1` if not opposing all other factions)
      - `oppose`: ID of win condition that is required to exist in the rolelist for this role to be rollable (Optional)
      - `color`: RGB value of role color
      - `targets`: List of role target data: (Optional)
        - `name`: Target name
        - `exclude`: List of entries to exclude from being rolled as a target
- `groups`: List of role groups:
  - `name`: Name of role group
  - `aliases`: List of possible aliases for group
  - `factions`: List of factions in group
  - `alignments`: List of alignments in group
  - `roles`: List of roles group

## Datasets

This repository has datasets for the following modes:

### Modern

- ToSA Standard: [`tosa-standard.json`](./tosa-standard.json)
- ToSA Standard + Chaos Roles: [`tosa-chaos.json`](./tosa-chaos.json)
- ToSA Tweaked: [`tosa-tweaked.json`](./tosa-tweaked.json)

### Legacy 1

- ToS1 Base: [`tos1-base.json`](./tos1-base.json)
- ToS1 Base + Expansion: [`tos1-ext.json`](./tos1-ext.json)
- ToS1 Base + Custom: [`tosa-legacy1-base.json`](./tosa-legacy1-base.json)
- ToS1 Base + Expansion + Custom: [`tosa-legacy1.json`](./tosa-legacy1.json)

### Legacy 2

- ToS2 Vanilla: [`tos2.json`](./tos2.json)
- ToS2 Vanilla + Custom: [`tosa-legacy2.json`](./tosa-legacy2.json)