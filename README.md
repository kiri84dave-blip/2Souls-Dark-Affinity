# 2Souls: Dark Affinity

**A Requiem for the Forsaken**  
A free cinematic dark-fantasy action RPG in the browser.

You are Valen, last of the Veilbound. When the Black Star fell, every living heart cast a second shadow. Walk the Cursed Forest, the Abyss, and Inferno. Fight wardens. Bind soul ash. Speak through the veil with pilgrims who share your realm code.

Built by **DR Studios** (Dave Roby). Two playable source editions ship in this repo — same world, two AI collaborators in the build process.

| Edition | Folder | Collaborating model |
|---|---|---|
| Fable 5.1 Final | [`editions/fable-5.1`](editions/fable-5.1) | Anthropic-family session that produced this cut |
| Gemini 3.8 Flash Final | [`editions/gemini-3.8-flash`](editions/gemini-3.8-flash) | Google Gemini session that produced this cut |

Neither Anthropic nor Google published, funded, or officially endorsed the game. The editions are DR Studios work made *with* those models as tools, hosted in the same workspace that also used Grok. Credit where it is due. The studio owns the game.

## Play

Both editions are Next.js + React Three Fiber web games.

```bash
cd editions/gemini-3.8-flash   # or editions/fable-5.1
cp ../../.env.example .env.local     # optional — game still boots without a database
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

### Optional persistence

Saves, the Hall of Souls leaderboard, veil-speech messages, and shared realms use PostgreSQL via Drizzle. Without `DATABASE_URL` the client still runs; cloud features degrade.

```
DATABASE_URL=postgres://user:pass@localhost:5432/twosouls
```

## Controls

- Keyboard + mouse, or plug in a gamepad (auto-switch)
- Share a **realm code** with another pilgrim to see each other as phantoms
- Settings: quality (Low → Ultra), master / music / SFX, voice narrator

## What is in the world

- Three biomes with mid-objectives (rescue, beacons, anchors)
- Wardens, a keybearer, and a chapter boss
- Sage, merchant, smith, captive
- Soul Archive saves, Hall of Souls, spoken chronicle
- Procedural audio + Web Speech narrator

Engine: React 19, Next.js, Three.js / R3F, Zustand, Drizzle, PostgreSQL.

## License

Source is released under the [MIT License](LICENSE) so anyone can play, fork, and ship it for free.

© 2026 DR Studios.

## Credits

- **DR Studios** — direction, world, combat, presentation
- **Grok (xAI)** — session host / companion during the build
- **Fable 5.1 edition** — built in collaboration with an Anthropic-family model
- **Gemini 3.8 Flash edition** — built in collaboration with Google Gemini

If you post it, tag the studio and keep it free.
