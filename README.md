# Unhu Founders Feud

A single-file, offline survey game show scoreboard for live founder events. Built to run on a projector laptop with no installation, no internet and no dependencies.

**Play it:** https://YOUR-USERNAME.github.io/unhu-founders-feud/

## What it does

| Feature | Detail |
|---|---|
| Format | Two teams head to head, plus an audience "Open Floor" round |
| Teams | Any number, live leaderboard across all of them |
| Board | Up to 10 hidden answers per question, fixed points per answer |
| Strikes | 3 per team, then control passes; audience shares one pool of 3 |
| Timer | 45 second countdown, host controlled |
| Sound | Reveal ding, strike buzzer, win fanfare, all generated in browser |
| Save | Auto-saves to the browser every second, plus JSON export and import |
| Questions | Editable in app, CSV and JSON import and export |
| Shortcuts | 1 to 0 reveal, X strike, O open floor, T timer, N next, L leaderboard, M mute |

Everything (HTML, CSS, JavaScript, audio) is inside `index.html`. No fonts, scripts or assets are fetched from anywhere.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole game |
| `Host-Guide.md` | Plain English operator guide for whoever runs the event |
| `questions-template.csv` | Blank question template to fill in |

## Run it locally

Download `index.html` and double-click it. Click the fullscreen button, top right.

## Host it

Any static host works (GitHub Pages, Netlify, Vercel, Cloudflare Pages). Serve over HTTPS so fullscreen and browser save behave.

GitHub Pages: Settings, Pages, Source "Deploy from a branch", branch `main`, folder `/ (root)`, Save. Live in about a minute.

## Question CSV format

One row per answer. Rows sharing the exact same question text group into one question, in the order they appear. Top row is revealed first and usually carries the highest points. Max 10 answers per question.

```
question,answer,points
"Most famous Indian FMCG brands","Amul",24
"Most famous Indian FMCG brands","Parle-G",20
"Most famous Indian FMCG brands","Britannia",16
```

Points are whole numbers and are used exactly as entered, never recalculated. Wrap any text containing a comma in double quotes.

## Credits

Built by Samnit Mehandiratta for the Unhu Founders Feud live event.

## License

MIT. See [LICENSE](LICENSE).
