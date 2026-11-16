# Imposter multiplayer party game

## Run locally
Requires Node.js 22+. From this folder:

```bash
npm install
npm start
```

Open http://localhost:3000. For real multiplayer across phones, deploy to a public host.

## Deploy to Render
1. Create a GitHub repository and upload these files (the files inside this folder, not the ZIP itself).
2. At https://dashboard.render.com choose New > Blueprint and connect the repository.
3. Confirm the web service from `render.yaml` and deploy.
4. Once deployed, use the public `.onrender.com` URL to create a room and share the generated invite link.

Notes: Rooms are stored in memory, so restarting the server clears rooms. Free hosting can sleep when idle, so the first visit may be slow. Run a single server instance (no horizontal scaling) because room state is not shared between instances. This is a prototype and is not production-hardened.

## Rules
Host selects any of 22 categories (550 words total), chooses 1–10 clue rounds and automatic/manual imposter count. At least 3 players are needed. A random starting player begins; clues proceed in the lobby's player order and repeat for each round. Voting starts automatically after the final clue. Every player votes once and the outcome is revealed when all votes arrive.
