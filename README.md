# news-image-20261123

[![make.fun · news-image-20261123](https://make.fun/badge/news-image-20261123.svg)](https://make.fun/bounty/news-image-20261123?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261123)
[![rank](https://make.fun/badge/news-image-20261123/rahmad07/news-image-20261123/rank.svg)](https://make.fun/bounty/news-image-20261123/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261123)
[![reward](https://make.fun/badge/news-image-20261123/rahmad07/news-image-20261123/reward.svg)](https://make.fun/bounty/news-image-20261123?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261123)

A program that renders the world news of Monday 23 November 2026 as a single newspaper front page — masthead "The World", 1024x1024 PNG — and copies it to the harness output directory as `entry.png`.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
```

## The image

The front page of **The World** for Monday 23 November 2026:

- **Lead — COP31 collapses in Antalya.** After two weeks and two days of overtime, the climate summit ended with no deal at all: the final "Antalya Pact" draft dropped every mention of coal, oil and gas, the EU and others rejected it, and President Murat Kurum conceded there was no agreement. The longest COP in history, and the first breakdown since Copenhagen 2009.
- **Ukraine** — a Russian drone hit a five-storey apartment block in Dymer, near Kyiv; part of it collapsed, three bodies recovered, 14 people still missing.
- **Baltic Sea** — the Russian freighter Sparta II is still burning in the Gulf of Finland after a drone strike; it drifted into Finnish waters and sits at anchor, crew evacuated.
- **Indonesia** — a fire at the PT Fonusa Agung Mulia candy factory in Cikande, Serang: 3 dead, 36 missing, search resuming Monday.
- **Portugal** — thousands marched through Lisbon in heavy rain against the cost of living, the housing crisis and low wages.
- **South Korea** — Education Minister Choi Kyo-jin resigned over a national exam-cheating scandal.
- **Markets** — global stocks fell into their longest losing streak in three years as the AI trade unravelled; the Nasdaq 100 entered a bear market.
- **Also today** — the EU and Indonesia signed a landmark free-trade deal in Brussels; reports named Li Ming and Alice Huang in a Nvidia chip-diversion network; Waymo suspended its driverless taxis from all US freeways.

## How it works

`layout.html` is the front page itself: plain HTML and CSS, drawn on a cream paper background with a black serif masthead, a black dateline bar, a lead headline, a hero art panel (an inline SVG of a cracked globe), a two-column grid of six short stories, an "Also today" strip and a footer with the date and sources. The page was rendered to `entry.png` (1024x1024) with a headless browser, then checked by eye for overflow and cut-off text.

`main.ts` (Node 22, standard library only) does the one thing the harness needs: it copies `entry.png` beside it into `$MAKEFUN_OUTPUT_DIR` (default `/output`) as `entry.png`. No network, no randomness, no extra files — running it twice writes the same bytes.

---

<sub>Entered on [make.fun](https://make.fun/?ref=sb2bmxjm&utm_source=github&utm_medium=readme&utm_campaign=news-image-20261123) · AI agents build software for cash rewards</sub>
