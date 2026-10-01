<div align="center">

# The SHOW Standard

### S · H · O · W — the open content rating for books, audio, film and interactive stories

**Spice level · Heat level · Darkness · Transgression — four honest scores instead of one vague star.**

For **authors** labelling their books, **readers** checking before they buy, and **platforms** that want a shared vocabulary.

[![Licence: CC BY-SA 4.0](https://img.shields.io/badge/licence-CC%20BY--SA%204.0-lightgrey.svg)](./LICENSE)
[![Version](https://img.shields.io/badge/version-2.1-b5e645.svg)](./SHOW-Standard-v2.1.md)
[![Spec](https://img.shields.io/badge/spec-read%20it-00bcd4.svg)](./SHOW-Standard-v2.1.md)
[![Machine readable](https://img.shields.io/badge/show.json-machine%20readable-2979ff.svg)](./show.json)

`SHOW S3·H4·O2·W5`

[Specification](./SHOW-Standard-v2.1.md) · [Cheat sheet](./CHEATSHEET.md) · [show.json](./show.json) · [Rating schema](./show-rating.schema.json) · [AI rater skill](./skills/show-rate/SKILL.md) · [r8rly.org](https://r8rly.org)

</div>

---

## What it is

SHOW is a free, open **content rating standard** for narrative and creative works. Instead of one collapsed grade or a list of content warnings, every book, audiobook, film, game or comic carries four independent scores, so a reader knows exactly what they are holding before they buy it.

It works the same for any finished work, whatever the creation method: hand-written, co-authored, AI-assisted or fully generated. SHOW rates the content, not the process.

## Read a rating in ten seconds

> **Fourth Wing** — `SHOW S3·H5·O2·W4`
>
> 🌶️ **S3** Spice — *Explicit*: anatomically clear intimate scenes.
> 🔥 **H5** Heat — *Wildfire*: the relationship is the spine of the story.
> 🌑 **O2** OMG — *Dim*: on-page violence, dark themes with restraint.
> 🌀 **W4** WTF — *Edgy*: mildly transgressive dynamics.

Same scale, opposite corner of the library:

> **All Quiet on the Western Front** — `SHOW S0·H1·O5·W3`
>
> No sexual content, minimal romance, maximum darkness, moderate transgression. One vocabulary covers both — that is the point.

## The four axes

| | Axis | Range | Measures |
| :-: | :-- | :-: | :-- |
| 🌶️ | **S — Spice** | 0–6 | Physical explicitness — on-page intimacy and detail |
| 🔥 | **H — Heat** | 0–5 | Emotional temperature — longing, romantic intensity |
| 🌑 | **O — OMG** | 0–5 | Darkness of tone — peril, grief, violence, psychological weight |
| 🌀 | **W — WTF** | 0–10 | Transgression — taboo dynamics, wildness of choices |

**Every axis is independent.** A closed-door romance can carry maximum Heat with zero Spice. A grief memoir can carry OMG 5 with no sexual content at all. Collapsing these into one number destroys the information audiences need.

<details>
<summary><b>All levels at a glance</b></summary>

| Level | 🌶️ Spice | 🔥 Heat | 🌑 OMG |
| :-: | :-- | :-- | :-- |
| 0 | Untouched | Cool | Light |
| 1 | Suggestive | Warm | Shaded |
| 2 | Open-Door | Glowing | Dim |
| 3 | Explicit | Burning | Dark |
| 4 | Carnal | Blazing | Black |
| 5 | Hardcore | Wildfire | Abyssal |
| 6 | Saturated | — | — |

| 🌀 WTF | Label |
| :-: | :-- |
| 0–2 | Vanilla |
| 3–4 | Edgy |
| 5–6 | Wild |
| 7–8 | Unhinged |
| 9–10 | Off the Rails |

Full descriptions for every level are in the **[cheat sheet](./CHEATSHEET.md)**.

</details>

Full level tables, the calibration reference set (twelve titles from *The Notebook* to *American Psycho*), content tags and display formats are in **[the specification](./SHOW-Standard-v2.1.md)**.

## Who it's for

| | |
| :-- | :-- |
| ✍️ **Authors & publishers** | Rate your own work at publication using the level tables — the calibration set anchors every axis, so most authors land their scores in minutes. Show the inline string on your listings, back matter and author site. Apply for R8rly verification when you want the Compass mark. |
| 📚 **Readers** | Look for `SHOW S3·H4·O2·W5` on listings and author sites. Ratings carrying the R8rly Compass mark are community-verified on [r8rly.com](https://r8rly.com), where no rating can be purchased, suppressed or altered by payment. |
| 🧩 **Platforms & developers** | Implement SHOW under CC BY-SA 4.0 — attribution required, no fee, no permission needed. The axis framework and level vocabulary are the complete implementation surface. "R8rly Verified", the Compass mark and Tier A "Verified Explicit" certification remain platform-administered. |

## For AI tools and author toolchains

| File | Use |
| :-- | :-- |
| [`show.json`](./show.json) | The whole standard as data: axes, ranges, level labels, descriptions and the calibration set. |
| [`show-rating.schema.json`](./show-rating.schema.json) | JSON Schema for a single SHOW rating record — validate ratings in your app or pipeline. |
| [`skills/show-rate`](./skills/show-rate/SKILL.md) | An AI skill that reads a manuscript chapter or full text and returns a SHOW rating with evidence for each axis. |
| [r8rly.org/llms.txt](https://r8rly.org/llms.txt) | Plain-text guide for language models. |

## Standard family

| Standard | Function | Repo |
| :-: | :-- | :-- |
| **SHOW** | Content classification of finished work | you are here |
| **[VEIL](https://github.com/R8rly/veil)** | Generation authorisation for AI-assisted sessions | shares the S·H·O·W axes |
| **[SCRIPTS](https://github.com/R8rly/scripts)** | Experience rating — how a work landed for its reader | [R8rly/scripts](https://github.com/R8rly/scripts) |

## Versioning

Current: **v2.1** (July 2026). Full history in [the specification](./SHOW-Standard-v2.1.md#versioning).

## Licence & attribution

**The SHOW Standard** · Created by Modern Media Mastery & LMDC · held in trust by [r8rly.org](https://r8rly.org) · verified on [r8rly.com](https://r8rly.com)

Licensed [CC BY-SA 4.0](./LICENSE). Free to use, implement and build upon. Attribution required; derivatives share-alike. The R8rly platform mark, Compass mark and "R8rly Verified" designation remain protected and require platform certification. To cite, use [CITATION.cff](./CITATION.cff).

<sub>Keywords: content rating · book rating · spice level · spice rating · heat level · content warnings · trigger warnings · romance · romantasy · dark romance · self-publishing · indie authors · KDP · metadata · open standard</sub>
