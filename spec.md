# Happy Birthday Aditi 🎉

## Current State

A 5-page birthday surprise web app with the following pages:
1. **CandleCeremonyPage** — 3 lit candles, tap each to blow out with 3-2-1 countdown, celebration sound (claps + hurray), then auto-navigates to page 2
2. **WelcomePage** — "Happy Birthday My Princess (Samta)" with fireworks, confetti, balloons, twinkling stars, cake image, Happy Birthday audio
3. **MemoriesPage** — 7 static photos with Hindi captions, numbered badges, Dropbox audio player
4. **MessagePage** — "Just For You 💖" with typewriter animation, floating hearts
5. **SurprisePage** — "Thank You" button triggers falling flower petals, fireworks, rose popup with "Once more Happy Returns of the Day, Cute Pie ❤️"

Photos are statically embedded in `/assets/uploads/`. All animations use CSS keyframes defined in `index.css`.

## Requested Changes (Diff)

### Add
- Nothing new

### Modify
- **Full rebuild** of the frontend — keep all content, logic, and data exactly as-is, but rebuild all component files from scratch cleanly with no bugs
- Ensure MemoriesPage photos always load (they are static local files at `/assets/uploads/`)
- Ensure audio player in MemoriesPage works with the Dropbox mp3 link
- Ensure page transitions are smooth (GPU-accelerated translate3d)
- Ensure typewriter on MessagePage auto-starts every time you visit that page

### Remove
- Nothing

## Implementation Plan

1. Rebuild `CandleCeremonyPage.tsx` — 3 candles, blow-out mechanic, 3-2-1 countdown flash, celebration audio (claps+hurray), auto-navigate onDone after 2.5s
2. Rebuild `WelcomePage.tsx` — fireworks canvas, confetti, stars, balloons, birthday cake emoji (🎂, NOT an image), glowing "Happy Birthday My Princess (Samta) 🎉🎂" title, Happy Birthday synthesized audio
3. Rebuild `MemoriesPage.tsx` — all 7 photos from `/assets/uploads/` with captions and numbered badges, Dropbox audio player with play/pause, progress bar, error handling
4. Rebuild `MessagePage.tsx` — "Dear My Aditi" typewriter letter, restarts on every visit, floating hearts
5. Rebuild `SurprisePage.tsx` — Thank You button, falling petals, rose emoji (🌹, NOT an image), fireworks, modal popup with message
6. Rebuild `PageNav.tsx` — 5 dots navigation, prev/next arrows
7. Keep `App.tsx` as-is (already clean with keep-alive page mounting)
8. Keep `index.css` as-is
9. Validate and fix any errors
