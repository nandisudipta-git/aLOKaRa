---
name: verify
description: Verify dotbro.in site changes by serving the folder locally and driving it in Chrome
---

# Verify dotbro.in site changes

Static HTML site — no build step. The Chrome extension blocks `file://`, so serve over localhost:

```bash
python3 -m http.server 8734   # run from this folder, in background
```

Then drive `http://localhost:8734/index.html` (landing) and `/feed.html` (the alge feed) with the claude-in-chrome tools.

## Flows worth driving
- Landing: scroll the card stack top to bottom — hero → why → how → principles → family → ronvey → footer. The companion dot should narrate each stop.
- Family section links deep-link into the feed: `/feed.html#study-gyaan`, `#life`, `#build-startup`, `#meet-people` — the matching legend item must show as active (white/bold).
- feed.html talks to live Supabase (project `fliheqjbwmcoggajovln`) — network required; header shows "N questions floating" when connected.

## Gotchas
- Hash-only navigation does not reload the page — feed has a `hashchange` listener; test both fresh-load and hash-change paths.
- Ghost text bleeding between cards mid-scroll is the intended "recede" effect, not a bug.
- Footer is `text-transform: uppercase`; the aLOKaRa span carries `style="text-transform:none"` to keep brand casing.
- **Deploy:** live site is Vercel (confirmed via `curl -sI https://dotbro.in` → `server: Vercel`), deployed via Vercel file-upload API — NOT git push, NOT GitHub Pages (old DEPLOY.md in ../www.dotbro.in is stale). See ../dotbro-in-PROJECT.md build log.
