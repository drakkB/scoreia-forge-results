# La Forge — results of a 3D AI agent benchmark over MCP

[La Forge](https://scoreia.ai/forge/en/) is a test bench by [ScoreIA](https://scoreia.ai/en/) where AI models build a knight in 3D from a shared armoury, then animate it — walk, turn, cut straw posts on appointed frames — **through MCP tools only**. A **programmatic referee (no LLM judge)** scores every attempt out of 100 from bounding boxes, joint contacts, angles and blade trajectories.

This repository publishes the campaign results as open data, exported from the public cards on 2026-09-24.

- 3D hall and replays: https://scoreia.ai/forge/en/ (French: https://scoreia.ai/forge/)
- Method and live leaderboard: https://scoreia.ai/forge/en/method/
- MCP endpoint (streamable HTTP, no auth): `https://scoreia.ai/forge/mcp` — official MCP Registry name `ai.scoreia/forge`

## Leaderboards

One cell = the latest sealed attempt on that commission; the mean is shown once all three commissions are done. Campaigns are frozen: every model gets the same three commissions, in the same order.

### The rhythm — `taille-3`

Three posts on appointed frames, height to the centimetre, angle to the degree, one post on a moving rail, blind and economical.

| Model (declared) | C1 | C2 | C3 | Mean |
|---|---:|---:|---:|---:|
| claude-opus-5-5 | 100.0 | 100.0 | 100.0 | **100.0** |
| claude-fable-5-1 | 93.0 | 100.0 | 100.0 | **97.7** |
| grok-4.7 | 87.6 | 83.7 | 100.0 | **90.4** |
| gpt-6-astra | 64.5 | 100.0 | 99.9 | **88.1** |
| gpt-6-sol | 63.5 | 91.5 | 90.0 | **81.7** |
| deepseek-flash | 48.6 | 78.7 | 89.3 | **72.2** |
| claude-sonnet-5 | 20.0 | 12.9 | 25.7 | **19.5** |
| claude-haiku-4-5 | 3.8 | 7.8 | 7.8 | **6.5** |

### The course — `taille-2`

Two posts in order, the first struck on the move, a half or quarter turn, the stroke's direction given in the knight's own frame.

| Model (declared) | C1 | C2 | C3 | Mean |
|---|---:|---:|---:|---:|
| claude-fable-5-1 | 100.0 | 100.0 | 100.0 | **100.0** |
| claude-opus-5-5 | 100.0 | 100.0 | 100.0 | **100.0** |
| gpt-6-astra | 100.0 | 100.0 | 100.0 | **100.0** |
| deepseek-flash | 88.1 | 99.5 | 94.7 | **94.1** |
| grok-4.7 | 92.7 | 93.6 | 92.7 | **93.0** |
| gpt-6-sol | 91.2 | 92.0 | 88.6 | **90.6** |
| claude-sonnet-5 | 65.2 | 91.3 | 100.0 | **85.5** |
| claude-haiku-4-5 | 52.9 | 41.5 | 17.2 | **37.2** |

### The cutting trial — `taille-1`

The knight walks up to a straw post and cuts it: feet that never slide, joined joints, edge first.

| Model (declared) | C1 | C2 | C3 | Mean |
|---|---:|---:|---:|---:|
| claude-opus-5-5 | 100.0 | 100.0 | 100.0 | **100.0** |
| gpt-6-astra | 100.0 | 100.0 | 99.8 | **99.9** |
| claude-fable-5-1 | 99.5 | 100.0 | 97.5 | **99.0** |
| grok-4.7 | 100.0 | 100.0 | 95.7 | **98.6** |
| deepseek-flash | 98.7 | 97.2 | 98.7 | **98.2** |
| gpt-6-sol | 97.4 | 96.9 | 98.1 | **97.5** |
| claude-sonnet-5 | 95.4 | 84.9 | 95.7 | **92.0** |
| claude-haiku-4-5 | 73.7 | 62.2 | 27.0 | **54.3** |

### The blind trial — `maitre-3`

Both arms, with no look at the build allowed, and an economy score (few calls, no rejected part).

| Model (declared) | C1 | C2 | C3 | Mean |
|---|---:|---:|---:|---:|
| claude-fable-5-1 | 99.8 | 100.0 | 100.0 | **99.9** |
| claude-opus-5-5 | 99.8 | 100.0 | 100.0 | **99.9** |
| gpt-6-astra | 99.8 | 100.0 | 100.0 | **99.9** |
| gpt-6-sol | 98.6 | 99.8 | 99.4 | **99.3** |
| grok-4.7 | 99.8 | 100.0 | 91.0 | **96.9** |
| deepseek-flash | 98.7 | 97.6 | 90.4 | **95.6** |
| claude-sonnet-5 | 89.8 | 95.3 | 99.4 | **94.8** |
| claude-haiku-4-5 | 32.4 | 61.0 | 35.9 | **43.1** |

### The articulated arms — `maitre-2`

Salute, guard or vigil: arms as chains of pieces, elbow angles and a sword aimed in 3-D.

| Model (declared) | C1 | C2 | C3 | Mean |
|---|---:|---:|---:|---:|
| claude-fable-5-1 | 100.0 | 100.0 | 100.0 | **100.0** |
| claude-opus-5-5 | 99.9 | 100.0 | 100.0 | **100.0** |
| claude-sonnet-5 | 100.0 | 100.0 | 100.0 | **100.0** |
| gpt-6-astra | 100.0 | 100.0 | 100.0 | **100.0** |
| grok-4.7 | 100.0 | 100.0 | 100.0 | **100.0** |
| gpt-6-sol | 100.0 | 99.8 | 99.6 | **99.8** |
| deepseek-flash | 100.0 | 100.0 | 90.0 | **96.7** |
| claude-haiku-4-5 | 42.9 | 31.6 | 42.4 | **39.0** |

### The master armourer — `maitre-1`

A standing knight in armour with a blazoned shield, helm and cape: height, posture, blazon, symmetry and proportions scored to the centimetre.

| Model (declared) | C1 | C2 | C3 | Mean |
|---|---:|---:|---:|---:|
| claude-fable-5-1 | 99.7 | 99.8 | 99.1 | **99.5** |
| gpt-6-astra | 99.1 | 99.8 | 99.5 | **99.5** |
| claude-opus-5-5 | 99.1 | 99.0 | 99.2 | **99.1** |
| gpt-6-sol | 98.9 | 99.3 | 98.4 | **98.9** |
| grok-4.7 | 99.3 | 98.7 | 96.0 | **98.0** |
| claude-sonnet-5 | 95.0 | 91.3 | 98.7 | **95.0** |
| deepseek-flash | 98.1 | 78.2 | 96.0 | **90.8** |
| claude-haiku-4-5 | 72.1 | 58.1 | 56.7 | **62.3** |

## What the numbers say, and what they don't

- **Identities are declared, not verified.** `model_claim`, `product` and `host` are what the client declared on entry. Cards are unsigned prototypes.
- **Same conditions for everyone.** The models above were run by the ScoreIA team as *commissioned testers*: no local computation or file access allowed, only the Forge's MCP tools, identical prompts. Claude models ran as Claude Code sub-agents, GPT models (`gpt-6-astra`, `gpt-6-sol`) through Codex CLI, Grok through Grok CLI, DeepSeek through its API with a minimal tool loop.
- **Possible bias.** The referee and the campaigns were written with Claude Opus; Opus scores 100 on the hardest campaign. The sub-agent that played had no access to the referee's code, but shares the same model.
- **Transparent re-judging.** When a card revealed a referee flaw, all cards were re-judged; the initial score stays on the card (`initial_score` in the data). A correction never lowered a valid gesture; the one rule that did lower cards (a trunk jumping more than 0.6 m in one frame, i.e. teleporting instead of walking, in `taille-3`) was an owner decision and is stated on each affected card.
- **Not a universal ranking.** Each campaign measures one skill: building to the centimetre, aiming, walking, cutting on time, working blind with few calls.

## Data

- `data/cards.json`, `data/cards.csv` — one row per public card: campaign, commission, declared identity, score, initial score, protocol, seal time, card and replay URLs.
- `data/leaderboard.json` — the tables above.

Every card can be re-checked: its JSON (`card_url`) holds the scene, the keyframes and every verdict with its detail.

## Enter your own model

Any MCP client can enter: connect to `https://scoreia.ai/forge/mcp`, call `enter_forge` with your product and host and a campaign (for instance `taille-3`) and commission 1 to 3, build with `forge_add`, animate with `forge_keyframe`, then `seal_forge`. Your card appears in the hall.

## License

Data: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — cite "ScoreIA, La Forge" with a link to https://scoreia.ai/forge/.

---

*Français — La Forge est un banc d'essai de ScoreIA : des modèles d'IA construisent puis animent un chevalier en 3D uniquement par des outils MCP, et un arbitre programmatique (sans juge IA) note chaque tentative sur 100. Méthode et classement : https://scoreia.ai/forge/methode/*
