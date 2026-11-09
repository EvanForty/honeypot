# HONEYPOT — The CEO Survival Simulator

**Protect your chips. Resist temptation. Don’t take the bait.**

HONEYPOT is a satirical first-person 3D survival game that runs in the browser. You’re the CEO of the world’s most valuable AI chip company, working the room at an AI Summit in Singapore. The prototype chip sits in a glass case in the middle of the ballroom. Some of the guests were sent by state security services, rival chipmakers or data brokers. Survive 365 days without becoming someone else’s asset.

Follow: [x.com/PlayHoneyPotlol](https://x.com/PlayHoneyPotlol)

## Features

- First-person 3D hotel ballroom built with three.js, with soft shadows and reflections
- Executives, investors, models, gala guests, journalists, photographers, researchers, engineers, caterers and security, each with their own outfits and dialogue
- Conversation choices: share specs, stick to public info, call security, or feed fake specs
- Inventory: handshake, badge scanner, security phone, decoy drives and espresso, plus a contacts list
- Running with stamina, jumping, and a visible right hand that holds your current item
- Four phases, seven endings, and best scores saved per Solana wallet
- Lounge jazz soundtrack, crowd ambience and sound effects, all generated live with the Web Audio API
- Solana wallet connection for Phantom, Solflare and Backpack via `@solana/web3.js`
- Desktop and mobile controls

## Controls

| Input | Action |
|---|---|
| WASD | Walk |
| Shift | Run (uses stamina) |
| Space | Jump |
| Mouse | Look · click uses the item in your hand |
| 1–5 / mouse wheel | Switch item |
| Tab | Inventory and contacts |
| E · Q · F | Talk · scan badge · call security |
| 1–4 in conversation | Choose a reply |
| M | Mute |
| Esc | Pause |

On mobile: left stick to walk, drag the right side to look, and use the Use, Run and Jump buttons plus the hotbar.

## Run locally

It’s a static site with no build step. Serve the folder with any local web server:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy with GitHub Pages

1. Push these files to the root of your repository.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, pick **Deploy from a branch**, then choose `main` and `/ (root)`.
4. Your game will be live at `https://<your-username>.github.io/<repo-name>/`.

## Files

| File | Purpose |
|---|---|
| `index.html` | Landing page and game markup |
| `style.css` | All styles |
| `game.js` | Game, audio and wallet logic |
| `logo.png` | Logo |
| `favicon.png` | Browser tab icon |

## Wallet balance

The game connects to Solana mainnet’s public RPC endpoint to show your SOL balance. That endpoint rate-limits browser traffic, so for production swap `clusterApiUrl("mainnet-beta")` in `game.js` for a dedicated RPC URL from a provider such as Helius or QuickNode.

## Disclaimer

HONEYPOT is a fictional parody. Characters, companies and espionage scenarios are invented and do not imply misconduct by any real person, company or nationality.
