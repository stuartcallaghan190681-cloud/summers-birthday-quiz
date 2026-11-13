# Summer’s 20th Birthday — Live Team Quiz

A real multiplayer birthday quiz for iPhones, Android phones and a host TV. Teams join with a six-character room code, submit answers, and get live results. Includes all 50 questions in five rounds.

## Publish online (required for playing on different phones)

1. Upload this project to a new GitHub repository.
2. At [render.com](https://render.com), create a **New Web Service**, connect the GitHub repository and choose the free instance (where available). Render should detect the included `render.yaml`; otherwise set build command `npm install` and start command `npm start`.
3. Wait for Render to give the service a public HTTPS URL. Open this URL in Safari on the host iPhone.
4. Tap **Host a new game**. Share the join link / room code with teams. Each team visits the same URL on their own phone.
5. Mirror the host iPhone to the TV using Control Centre → Screen Mirroring (AirPlay-compatible television or Apple TV required). The host reveals questions, awards points and advances the quiz.

Note: this runs as a Node server. Opening `index.html` directly from the Files app will **not** support shared play. Free hosted servers may sleep when unused and can restart, clearing the game. Keep the host page open. The host token and team identity are saved in the current tab session only.

## Local test

```bash
npm install
npm start
```
Open http://localhost:3000. Other devices must use the machine's accessible LAN IP (not localhost).

## Quiz rules

For factual rounds, award one point per correct answer. For family/roast rounds, Summer awards points. The game doesn't mark open-text answers automatically: the host decides and taps +1 for teams who earned a point. Teams can edit their answer only before they submit (one submission per team per question). Host can navigate backwards and forwards, and can restart the game. Scores live in server memory, not a database.
