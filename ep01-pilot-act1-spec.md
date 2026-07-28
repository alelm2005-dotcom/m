# EP 01 — ACT-1 PILOT — Execution Spec
### Seedance 2.0 · 1080p std · 16:9 · 9 blocks · 0:00–1:30 · Faceless

**Purpose:** validate style key, faceless treatment, and VO pacing before committing
~4,300 credits to the remaining 39 blocks.

**Status:** blocked on funding. Balance 2.8 credits. Needs ~838. Authorized cap: 900.

---

## Budget against the 900 cap (preflighted rates)

| Item | Unit | Qty | Total |
|---|---|---|---|
| Seedance 2.0 clip, 10s @ 1080p std | 90 | 9 | 810 |
| Reference stills (seedream_v5_pro) | 3 | 8 | 24 |
| VO lines (seed_audio) | 0.4 | 9 | 3.6 |
| **Total** | | | **837.6** |
| Headroom under cap | | | 62.4 |

### ⚠ Retry exposure
A single failed/rejected clip costs **90** to redo — more than the 62.4 of headroom.
The 9-block plan has **no retry budget**. Two ways to handle it:

- **9 blocks (1:30), 837.6** — full plan, but one bad block breaches the cap by ~28.
- **8 blocks (1:20), 747.6** — drops B09, leaves 152.4 = one clean retry in budget.

Recommended: run 9 and accept that one failure needs ~90 more, since the 9th block
(the "yacht named Boat" laugh line) is the pilot's best test of comic timing.

---

## Why these 9 blocks
The pilot deliberately spans every visual mode the full episode needs, so nothing
is left unvalidated:

- **Epic desert/caravan** (B01) — the signature look
- **Faceless human insert** (B02) — validates the hands-only treatment of the 👤 beats
- **Motion-graphic / map** (B04, B06) — the debunk act leans on this
- **Comedy insert** (B08) — the salt gag, tests whether visual humour lands
- **Interior/throne** (B09) — character staging without a face

If all five modes read well, the remaining 39 blocks are variations on them.

---

## GLOBAL STYLE KEY (byte-identical in every prompt)
> "Cinematic historical documentary style, golden-hour desert palette (deep amber, burnt
> sienna, lapis night blues), volumetric dust light, painterly photoreal texture like a
> prestige streaming docudrama, 14th-century West African empire, no text, no watermarks,
> no modern objects."

Every clip: `duration:10`, `resolution:"1080p"`, `mode:"std"`, `aspect_ratio:"16:9"`,
camera always moving, **no identifiable faces in close-up** (faceless format).

---

## REFERENCE STILLS (generate first, approve, then reuse as `image_references`)
| # | Asset | Aspect | Used by |
|---|---|---|---|
| R1 | Style key anchor | 16:9 | all |
| R2 | Sahara dunes at dawn, caravan route | 16:9 | B01, B04 |
| R3 | Medieval Cairo skyline, minarets | 16:9 | B01, B03 |
| R4 | Desk set — manuscripts, coffee cup, warm lamp | 16:9 | B02, B05 |
| R5 | Gold dust / coin prop (through-line) | 1:1 | B03, B07 |
| R6 | Salt slab prop | 1:1 | B07, B08 |
| R7 | Glowing map of Mali / Niger river | 16:9 | B06 |
| R8 | Mali throne room interior | 16:9 | B09 |

---

## BLOCK MAP — 9 × 10s

**B01 · 0:00–0:10** — VO: "In the summer of 1324, one tourist walked into Cairo... and crashed its economy for the next twelve years."
SCENE: Vast golden caravan emerging from heat-shimmer mirage on the Sahara horizon at dawn, thousands of silhouetted figures and camels, slow aerial push-in, gold dust glinting in the air. Hard cut on "crashed" to medieval Cairo skyline as golden light floods the frame.
REFS: R2 → R3 → R1

**B02 · 0:10–0:20** — VO: "Not with an army. Not with a scheme. He did it by being generous."
SCENE: Anonymous hands place a coffee cup beside research papers and old manuscripts on a wooden desk, warm lamp light, slow overhead drift. Papers show hand-drawn maps and figures, illegible. No face, no torso above the wrists.
REFS: R4 → R1

**B03 · 0:20–0:30** — VO: "And the famous number attached to his name — richest man ever, four hundred billion dollars — is completely made up. I checked."
SCENE: A colossal shimmering gold numeral hangs over a dark desert, then crumbles into falling sand and gold dust. Slow low-angle push. Ends on a single coin spinning to rest.
REFS: R5 → R2 → R1

**B04 · 0:30–0:40** — VO: "So: who was he? How rich was he actually? I did the math three ways, and the results are absurd."
SCENE: Three fast hard cuts — a golden African map igniting at Mali; an overflowing merchant's scale tipping; a ruined desert city half-swallowed by dunes. Each cut a different shot size (wide → close → high angle).
REFS: R7 → R5 → R2

**B05 · 0:40–0:50** — VO: "And why does nobody remember his empire? That last part is the one that got me."
SCENE: Slow pull-back from the lamplit desk and its scattered manuscripts into surrounding darkness, papers stirring. Contemplative, quiet, no hands in frame.
REFS: R4 → R1

**B06 · 0:50–1:00** — VO: "West Africa, early 1300s. While Europe was busy dying of... basically everything, the Mali Empire controlled the two most ridiculous cash cows of the medieval world."
SCENE: Map of Africa glowing gold at Mali, camera dives toward the Niger River; split-tone transition from cold grey plague-era Europe to warm thriving golden Mali.
REFS: R7 → R1

**B07 · 1:00–1:10** — VO: "Gold... and salt. Yes, salt. In the Sahara, salt traded — at times, weight for weight — with gold."
SCENE: A merchant's balance scale, slab of white salt on one pan, gold dust on the other, holding perfectly level. Slow orbit, dust motes in shafts of light.
REFS: R6 → R5 → R1

**B08 · 1:10–1:20** — VO: "The seasoning on your fries used to be a currency. Let that sink in."
SCENE: Comedy insert — anonymous hand sprinkles real salt beside a gleaming gold ingot on dark stone, deadpan static-ish macro with slow drift. No face.
REFS: R6 → R5 → R1

**B09 · 1:20–1:30** — VO: "Running this machine: Mansa Musa the Ninth. 'Mansa' means king — so his name is literally 'King Musa.' The medieval equivalent of naming your yacht 'Boat.'"
SCENE: Wide of a Mali throne room, a robed ruler seen only from behind, silhouetted against a bright arched window, attendants in soft focus. Slow reverent push-in that lands on the joke's beat.
REFS: R8 → R1

---

## VOICEOVER
One locked voice for all 9 lines (user picks from library at kickoff) — English,
confident, dry-witted documentary register. Lines sized 14–26 words to fill ~9.5s
without rushing. Script's written pauses (وقفة) preserved.

## EXECUTION ORDER (on funding)
1. Voice pick + generate R1 style key → approve.
2. Generate R2–R8 (7 stills, parallel) → approve.
3. Fire 9 Seedance clips in parallel batches of ≥4, poll to terminal.
4. Generate 9 VO lines with the locked voice.
5. Assemble to one 1:30 1080p MP4 → deliver + push reference to PR #1.
6. Review → decide on the remaining 39 blocks (~4,300).
