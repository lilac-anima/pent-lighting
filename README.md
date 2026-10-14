# Penthouse Lighting

Local Philips Hue inventory and coordinated lighting effects.

## Current inventory

The Hue Bridge inventory is stored in [`inventory/lights.json`](inventory/lights.json), with a readable summary in [`inventory/lights.md`](inventory/lights.md).

- 17 color-capable lights
- 7 rooms: Bedroom, Bathroom, Den, Kitchen, Living room, Front door, Hallway
- 1 Home zone
- 1 Entertainment configuration (`Music area`)
- 54 API v2 scenes / 63 legacy API scenes
- 13 sensors

## Location map

- **Bedroom:** Bed Left, Bed Right
- **Bathroom:** Hue color lamp 1–3
- **Den:** Den Overhead 1–2, Couch Corner, Couch Left, Couch Right, TV Left, TV Right
- **Kitchen:** Kitchen Overhead 1–2
- **Living room:** Living Room Overhead
- **Front door:** Entry Overhead
- **Hallway:** Hallway

## Local credentials

`.hue-credentials.json` contains the local Bridge application credential and is intentionally ignored by Git. Never commit or share it. The Bridge IP is recorded in the inventory for local discovery, but credentials must be recreated on another computer.

## Working on another computer

1. Clone this repository.
2. Install a Hue API v2 client or use the local Bridge API.
3. Pair the new computer by pressing the physical button on the Hue Bridge.
4. Generate a new local application credential; do not copy the credential file into a public location.
5. Refresh the inventory if the lighting setup has changed.

The first implementation should preserve the logical room/group names above and build effects on top of them rather than hardcoding only individual bulb IDs.
