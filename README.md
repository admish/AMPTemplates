# XGA Custom AMP Templates

Custom [AMP](https://cubecoders.com/AMP) Generic-module templates for the XGA.io game server host. Registered in AMP as a custom configuration repository so these survive official template fetches.

## Templates

### GatekeeperV3 Bot

The Gatekeeper Discord bot ([leonbreidenbach-pc/GatekeeperV3](https://github.com/leonbreidenbach-pc/GatekeeperV3) fork), removed from the official AMPTemplates repo. Files:

- `gatekeeperv3.kvp` — template manifest (entry point)
- `gatekeeperv3config.json` — instance settings shown in the AMP UI (tokens/credentials are entered per-instance, never stored here)
- `gatekeeperv3metaconfig.json` — maps settings into the bot's `tokens.py`
- `gatekeeperv3ports.json` — port definitions
- `gatekeeperv3updates.json` — update stages (fetches the bot from the fork, builds a Python venv)

## How AMP consumes this repo

In the ADS panel: **Configuration → Instance Deployment → Configuration Repositories → Add** → `admish/AMPTemplates`, then **Fetch Latest**. AMP pulls this repo alongside the official CubeCoders/AMPTemplates on every fetch — no manual re-cloning, no clobbering.

Files must stay flat in the repo root (same layout as the official AMPTemplates repo).
