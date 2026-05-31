# What is UnicodiaSesh?

**In a nutshell:** it is a Unicode 18 font for Egyptian hieroglyphs based on JSesh.
- The nicest JSesh-based font ever. Why — see below.
- The widest coverage among free and semi-free fonts. The only catch: 568 NewGardiner’s tofu are extended (refused by policy), and all UnicodiaSesh’s tofu are core.

In my humble software called Unicodia, it used to be just a “gag font” for Egyptian hieroglyphs. Even in that state, it was taken to various sites. But when I started checking/fixing existing glyphs and drawing new ones, it became clear that it might be the new standard for Egyptian fonts: at the time of writing, more than 1’000 hieroglyphs are modified.

The font is semi-free, see license. Well, that’s the really old man at JSesh.

Software maturity index: **5 (production/stable)**. With coverage of the main block (13000), it is now usable for a general audience.

# What makes UnicodiaSesh so special?

☂️ **Coverage.** The initial version covered 2930/3995 of block A. When I finished the main block, the A’s coverage was 3349/3995. For personal reasons, I cannot work on USesh as much, and coverage stopped at 3600. Again, the main block is fully covered.

🤖 **Synergy of automation and handwork.** The font started as an automated script that worked around FontForge’s bugs, but a lot of handwork made it usable outside Unicodia. Everything is checked, and you wouldn’t find Ptah with a curved beard, long before Rosmorduc did this in JSesh.

👥 **Consistency.** It was not the strength of JSesh. One example: all open booths O22 now have the same style.

🔢 **Counting marks.** All counting marks are done from scratch; only the largest (e.g. 9 flowers) have a separate style. It is not a font for an Egyptian word processor, it’s a general-use Unicode font, right?

💄 **Beauty.** It’s actually the strength of JSesh, but the real beauty is in extensions, and I scour through them manually.

🐜 **Small pitches.** JSesh’s black arms are a miracle. And I address other troubles: I exaggerate props, I prefer thick lines to double.

📖 **Unique way of combining hieroglyphs and text.** Short hieroglyphs are aligned with the baseline, tall ones go a bit down. Maybe it is not historically accurate, but it surely saves space.

🗳 **“Voting”.** This simple policy — if image and description contradict, NewGardiner decides — makes UnicodiaSesh a compromise between Unicode compliance and usability for specialists.

# FAQ

**Why are lost signs put this way?**

Because short hieroglyphs are put this way. Lost signs — surprise — are just totally unreadable hieroglyphs. They are just a little bit bigger than an average hieroglyph.

# Stability policy

The author provides no stability. Everything may change, including bearings, line height, character styles, etc. For exact text layout, freeze the version.

# Quality policy

* Legacy:
  * Equiv. sequence = some core: invent a difference
  * Equiv. sequence = flipped/combination: normal quality
* No description (mostly extended): just vaguely resembles the sample image
* Same if the sample image is not in harmony with the description, but just for details that are not in harmony. I use the “rule of vote”: the NewGardiner font decides what’s right
  * NewGardiner is a greater vote: if all three contradict, take NewGardiner’s
  * Every detail is checked separately
* Short-haired man has no beard unless specified
* Other men may have any beard except god’s unless specified
* Described but really small detail (ankh in the hand…) = thing of lower importance, fix if the hiero was touched for another reason.
  * In hieros drawn/touched by us, such details are really exaggerated.
* The difference between duck and goose is ephemeral, there are no efforts to make them distinct. However, their necks are light.
* If the hieroglyph is not extensively disunified, any confirmed image is suitable. Example: female acrobat bending backwards 13744=B37a, took B37 and consider OK
* Cases whose inconsistency is NOT an issue:
  * Far apart: e.g. human and donkey.
  * Big and small: e.g. a detailed crown and the same crown on a king.

# Roadmap

- The first working version. ☂️ ≈2930/3995 ✅ autumn 2024
- Phase 1. Together with NewGardiner, 100% coverage. ☂️ ≈2950/3995 ✅ May 2025
- Phase 2. Check all glyphs, maturity 3. ☂️ ≈3200/3995 ✅ September 2025
- Phase 3. Cover the main block, maturity 5. ✅ November 2025
- Mini-task 3a. Create stubs of special characters. ☂️ 3359/3995 ✅ November 2025
- Milestone 3b. Beat NewGardiner in coverage. ✅ December 2025
- Phase 4. Move to Unicode 18. ☂️ 3575/3995 ✅ February 2026
- **Mini-task 4a. Track and draw ninja changes of Unicode 18.** ☂️ 3580/3995 ✅ February 2026
- Mini-task 4b. Write a formal TSV on each Unicode character, to allow someone to implement a JS-based formatter: A-B-C values, Y boundaries, Unicode info, license for glyph
- Mini-task 4c. Lay marks of damaged hashes. An interesting programmer’s task that won’t bloat the font much.
- ??? Special version that supports mirrored characters (unneeded for Unicodia, 2× bigger)
- ??? Make the build process less path-dependent

Probably WILL NEVER support full formatting.

# How to build

1. Need software: FontForge, Inkscape, TtfAutoHint
2. Put JSesh SVGs tn the ``svg`` directory. WARNING: those SVGs are non-versioned
3. Open UnicodiaSesh.sfd
4. Run script (Ctrl+Period) load-glyphs.py
5. Wait REALLY long, approx 30m
6. DO NOT SAVE
7. Check sesh.log, it might show problems
8. The longest operation, SVG uniting, will be cached, and the next runs will be shorter

# If you want to repeat precisely

- FontForge Oct 2025
- Inkscape 1.4.2
- TtfAutoHint 1.8.4
- JSesh 7.9.1

# How to develop?

See [develop.md](develop.md).
