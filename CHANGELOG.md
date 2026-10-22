# Changelog

## 1.0.0 — 2026-10-22

First release.

- **Audit a short-form video in the Gemini app.** Upload a finished video and get a scorecard for seven dimensions (hook, pacing, clarity, sound, proof, engagement, platform fit), an overall score, the retention risk and ranked fixes with timecodes.
- **Three detail levels:** 1 Quick (plain language, three fixes, one better opening line), 2 Standard (scorecard, top fixes, three alternative hooks) and 3 Pro (everything, in editing terms). Without a level in your message, Gemini asks only the level question and waits; it keeps that level for the rest of the chat.
- **Your defaults:** four lines at the top of the skill (`Default level`, `Default language`, `Default niche`, `Default platform`). Change them on Gemini's Skills page to skip the level question, fix the report language, or judge every video against your niche and platform.
- **Technical and platform check** for Instagram Reels, TikTok and YouTube Shorts: duration rules (including the worldwide block of Shorts over 1:00 with a Content ID claim), 9:16 framing, black bars, blank first or last frames, ungraded Log or HDR footage, and captions inside the areas the app covers with buttons and text.
- **Sound checked by ear:** voice-to-music balance, volume jumps between cuts, cut-off sentence endings and clipping. LUFS and dB values are editing targets, not measurements.
- **How to tell if it worked:** the fixes end with the numbers to check after publishing and how to compare them fairly with your own recent videos. No target numbers, no predictions.
- **Experiments:** one or two techniques the video doesn't use yet, labelled "Experiment": worth testing, not a proven fix. Always exactly three alternative hooks.
- **Honest about what Gemini can observe:** timecodes to the second, N/A instead of a guessed score, no overall score when a dimension is N/A, no hunting for single AI glitches in frames, and a one-line privacy note.
- **Install by upload:** download `SKILL.md` from the release and upload it on Gemini's Skills page. `manual-setup.txt` (also in the release) is the fallback for creating it manually.
- **Tested** in the Gemini web app by Cutting Clockwork (13 to 18 October 2026): upload of the single `SKILL.md`, the level question and the default lines, report language, privacy note, experiments, the "How to tell if it worked" paragraph and exactly three hooks.
