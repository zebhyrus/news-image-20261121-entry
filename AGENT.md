# Build note — news-image-20261121-entry

## What the image shows

A one-page newspaper front page, "THE WORLD", dated SATURDAY 21 NOVEMBER 2026.
It sums up the world news of 21 November 2026 in six stories: one hero plus five
others, across Latin America, Europe, the United States, and Asia.

## The 6 stories

1. HERO — 6.8 QUAKE SHAKES PERU: a magnitude 6.8 earthquake struck the Andean
   region of Junin, Peru, at 129 km deep; tremors were felt in Lima, residents
   took to the streets and lawmakers left Congress; no casualties or major
   damage were reported and there was no tsunami threat.
2. Russian missiles crash in Poland: a Kh-101 cruise missile came down near
   Nowy Lipowiec during the Koalicja 2026 allied exercise; PM Donald Tusk
   called it a deliberate provocation; no injuries.
3. Tech sell-off drags markets lower: a broad tech stock sell-off pulled
   markets down, with Anthropic shares sliding.
4. Mamdani: Rikers to close by 2032: New York Mayor Zohran Mamdani unveiled
   the city's first full plan to close the Rikers Island jail complex by 2032.
5. India draws record foreign cash: foreign investors poured a record
   Rs 1.22 lakh crore into Indian shares in November, the biggest monthly
   inflow ever, per depository data.
6. Gen Z rallies sweep Europe: thousands marched in 25 countries over living
   costs, military spending and the climate.

## How it was built

- Stories were researched with web news search on the morning of 21 Nov 2026
  (UTC day young, so coverage is Asia-Pacific plus overnight developments);
  every fact above is taken from those search results, nothing invented.
- The front page was authored fresh as SVG (`entry.svg`) in this session:
  masthead, dateline, hero headline with a hand-drawn seismic trace band,
  three-column row, two-column row, footer.
- Rendered to 1024x1024 PNG with headless Chrome:
  `--headless --disable-gpu --no-sandbox --screenshot=entry.png
  --window-size=1024,1024 entry.svg`, then read back and checked for
  legibility (headlines readable, no garbled or cut-off text).
- `main.ts` (Node 22, stdlib only) copies `entry.png` to
  `$MAKEFUN_OUTPUT_DIR/entry.png`.
