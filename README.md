# What is UnicodiaSesh?

**In a nutshell:** it is a Unicode 17 font for Egyptian hieroglyphs based on JSesh.
- The nicest JSesh based font ever. Why — see below.
- The widest coverage among free and semi-free fonts. The only catch: 568 NewGardiner’s tofu are extended (refuses by policy), and all UnicodiaSesh’s tofu are core.

In my humble software called Unicodia, it was just a “gag font” for Egyptian hieroglyphs. Even in that state it was taken to various sites. But when I started to check/fix existing glyphs and draw new, it became clear that it might be the new standard for Egyptian font: at the moment of writing, more than 1’000 hieroglyphs are modified.

The font is semi-free, see license. Well, that’s the really old man at JSesh.

Software maturity index: **5 (production/stable)**. With coverage of the main block (13000), it is usable for general audience now.

# What makes UnicodiaSesh so special?

☂️ **Coverage.** The initial version covered 2930/3995 of block A. When I finished the main block, the coverage of A was 3349/3995.

🤖 **Synergy of automation and handwork.** The font started as an automatic script that worked around FontForge’s bugs, but lots of handwork made it usable outside Unicodia. Everything is checked, and you wouldn’t find Ptah with curved beard — long before Rosmorduc did this in JSesh.

👥 **Consistency.** It was not the strength of JSesh. One example: all open booths O22 now have the same style.

🔢 **Counting marks.** All counting marks are done from scratch, only the biggest (e.g. 9 flowers) have a separate style. It is not a font for Egyptian word processor, it’s a general-use Unicode font, right?

💄 **Beauty.** It’s actually the strength of JSesh, but the real beauty is in extensions, and I scour through them manually.

🐜 **Small pitches.** JSesh’s black arms are a miracle. And I address other troubles: I exaggerate props, I prefer thick lines to double.

📖 **Unique way of combining hieroglyphs and text.** Short hieroglyphs are aligned to baseline, tall ones go a bit down. Maybe it is not historically accurate, but surely saves space.

🗳 **“Voting”.** This simple policy — if image and description contradict, NewGardiner decides — makes UnicodiaSesh a compromise between Unicode compliance and usability for specialists.

# FAQ

**Why are lost signs put this way?**

Because short hieroglyphs are put this way. Lost signs — surprise — are just totally unreadable hieroglyphs. They are just a little bit bigger than average hieroglyph.

# Stability policy

The author does not provide any stability. Everything may change, including bearings, line height, character styles etc. For exact text layout, freeze the version.

# Quality policy

* Legacy:
  * Equiv. sequence = some core: invent a difference
  * Equiv. sequence = flipped/combination: normal quality
* No description (mostly extended): just vaguely resembles the sample image
* Same if the sample image is not in harmony with description, but just for details that are not in harmony. I use the “rule of vote”: the NewGardiner font decides what’s right.
* Short-haired man has no beard unless specified
* Other men may have any beard except god’s unless specified
* Described but really small detail (ankh in the hand…) = thing of lower importance, fix if the hiero was touched for another reason.
* The difference between duck and goose is ephemeral, no efforts to make them distinct. However, their necks are light.
* If the hieroglyph is not extensively disunified, any confirmed image is suitable.
* Cases whose inconsistency is NOT an issue:
  * Far apart: e.g. human and donkey.
  * Big and small: e.g. crown in high detail and the same crown on a king.

# Roadmap

- The first working version. ☂️ ≈2930/3995 ✅ autumn 2024
- Phase 1. Together with NewGardiner, 100% coverage. ☂️ ≈2950/3995 ✅ May 2025
- Phase 2. Check all glyphs, maturity 3. ☂️ ≈3200/3995 ✅ September 2025
- Phase 3. Cover main block, maturity 5. ✅ November 2025
- Mini-task 3a. Create stubs of special characters. ☂️ 3359/3995 ✅ November 2025
- **Milestone 3b.** Beat NewGardiner in coverage. ✅ December 2025
- Mini-task 3c. Lay marks of damaged hashes. An interesting programmer’s task that won’t bloat the font very much.
- ??? Special version that supports mirrored characters (unneeded for Unicodia, 2× bigger).
- ??? Make build process less path-dependent

Probably WILL NEVER support full formatting.

# How to build

1. Need software: FontForge, Inkscape, TtfAutoHint
2. Put JSesh SVGs to Svg directory. WARNING: those SVGs are non-versioned
3. Open UnicodiaSesh.sfd
4. Run script (Ctrl+Period) load-glyphs.py
5. Wait REALLY long, approx 30m
6. DO NOT SAVE
7. Check sesh.log, it might show problems
8. The longest operation, SVG uniting, will be cached, and next runs will be shorter

# If you want to repeat precisely

- FontForge Oct 2025
- Inkscape 1.4.2
- TtfAutoHint 1.8.4
- JSesh 7.9.1

# How to develop?

See [develop.md](develop.md).
