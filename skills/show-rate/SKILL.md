---
name: show-rate
description: Rate a manuscript, chapter, book, script or story with the SHOW Standard v2.1 — spice level (S 0–6), heat level (H 0–5), darkness (O 0–5) and transgression (W 0–10). Returns the inline rating "SHOW S3·H4·O2·W5" with evidence for each axis and suggested content tags. Use for authors, editors and publishers labelling romance, romantasy, dark romance and any narrative work.
license: CC-BY-SA-4.0
---

# SHOW Rater

Rate the supplied text with **The SHOW Standard v2.1** (CC BY-SA 4.0 · Modern Media Mastery & LMDC · held in trust by r8rly.org). The standard is in `show.json` and `SHOW-Standard-v2.1.md` in this repository. Use only its level tables. Do not add levels, rules or adjustments of your own.

## Steps

1. Read the full text supplied.
2. Rate each axis **on its own**. No axis modifies any other.
   - **S — Spice (0–6):** physical explicitness, on-page intimacy and detail.
   - **H — Heat (0–5):** emotional temperature, longing, romantic intensity.
   - **O — OMG (0–5):** darkness of tone, peril, grief, violence, psychological weight.
   - **W — WTF (0–10):** transgression, taboo dynamics, wildness of content choices.
3. For each axis, pick the level whose description in the table matches what is on the page. Check against the calibration set in `show.json` (for example *The Notebook* S1·H5·O2·W1, *Fourth Wing* S3·H5·O2·W4).
4. Note specific content types as content tags (for example: on-page violence, forced proximity, morally grey protagonist). Tags go beside the scores, never into them.

## Spice levels

| 0 Untouched | 1 Suggestive | 2 Open-Door | 3 Explicit | 4 Carnal | 5 Hardcore | 6 Saturated |
| :-- | :-- | :-- | :-- | :-- | :-- | :-- |
| Kissing only. Door fully closed. | Fade-to-black, implied intimacy. | On-page intimacy with discretion. Sensation over anatomy. | Anatomically clear, multiple scenes. | High-frequency explicit scenes. Intimacy is load-bearing. | Kink, BDSM, power exchange at standard intensity. | Explicit intimacy is the dominant content. |

## Heat levels

| 0 Cool | 1 Warm | 2 Glowing | 3 Burning | 4 Blazing | 5 Wildfire |
| :-- | :-- | :-- | :-- | :-- | :-- |
| Romance incidental or absent. | Affection, light flirtation. | Attraction acknowledged. Lingering looks, first kisses. | Slow-burn intensity. Yearning. | Vulnerable confessions, soul-bared scenes. | The relationship is the spine of the story. |

## OMG levels

| 0 Light | 1 Shaded | 2 Dim | 3 Dark | 4 Black | 5 Abyssal |
| :-- | :-- | :-- | :-- | :-- | :-- |
| Sweet, cozy, comedy, family. | Mild angst, mild peril. | On-page violence, dark themes with restraint. | Captivity, stalker, trauma, MC/mafia, war. | Transgressive, dub-con, brutality. | Extreme — content-warning gated. |

## WTF levels

| 0–2 Vanilla | 3–4 Edgy | 5–6 Wild | 7–8 Unhinged | 9–10 Off the Rails |
| :-- | :-- | :-- | :-- | :-- |
| Conventional, no taboo. | Mild transgression, age gap. | Step-relationships, captivity-coded, antihero. | Strong taboo, dub-con romantically framed. | Non-con as central trope, extreme taboos. |

## Output

```
SHOW S3·H4·O2·W5

S3 Spice — Explicit: <one line of evidence from the text>
H4 Heat — Blazing: <one line of evidence>
O2 OMG — Dim: <one line of evidence>
W5 WTF — Wild: <one line of evidence>

Content tags: <tag>, <tag>, <tag>
Rated text: <title / chapter supplied>
```

Also return the rating as JSON matching `show-rating.schema.json`:

```json
{"standard":"SHOW","version":"2.1","S":3,"H":4,"O":2,"W":5,"tags":["forced proximity"],"display":"SHOW S3·H4·O2·W5","rated_by":"author","verified":false}
```

This is a self-rating. "SHOW Verified" and the R8rly Compass mark are given only through community verification on [r8rly.com](https://r8rly.com) — never write "Verified" in the output.
