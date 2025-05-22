### Automation blueprint: duck playing players volume in area, where satellite is active.

This automation will adjust volume on all players in area to given level (by default 20%), when satellite starts listening. After returning to idle, volume will be restored.

To avoid ducking volume on the active satellite, automation will skip media player of satellite itself, including one connected via Music Assistant, if it's present.
Also it will still handle commands like "volume up" on playing media players. Example:
- "player 1" is playing media on volume 55%;
- user commands "hey Jarvis";
- "player 1 volume reduced to 20% (and remembers the initial offset, 35%);
- user commands "volume up on player 1";
- HA is increasing volume on "player 1" to 30%;
- after interaction with satellite finished, "player 1" volume is raised to 65% by applying previous offset 35%.

  
[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2FFutureProofHomes%2FSatellite1-HA-Automations%2Frefs%2Fheads%2Fmain%2Fblueprints%2Fautomation%2FFutureProofHomes%2Fduck_area_players_for_satellite.yaml)
