# Gemini Video Audit

Get honest, specific feedback on a short-form video before you publish it. Drag the video into Gemini, and get back:

- a scorecard for hook, pacing, clarity, sound, proof, engagement and platform fit;
- a technical and platform check (Instagram Reels, TikTok and YouTube Shorts duration rules, 9:16 safe zones for captions, and audio loudness & mix quality);
- the top fixes, ranked by impact, with timecodes;
- alternative hooks, and at the Pro level a rewritten voice-over and a 9:16 shot list.

You choose how detailed the report is: **1 Quick** (plain language, three fixes), **2 Standard** (scorecard, top fixes and three alternative hooks) or **3 Pro** (everything, in editing terms).

The score is editorial feedback, not a prediction. The skill does not forecast views and cannot tell you whether a video will go viral.

This is a skill for the **Gemini app** (web and desktop). No editing software, plugins or coding needed.

<!-- TODO: screenshot of a real scorecard, e.g. docs/scorecard.png -->

Made by [Cutting Clockwork](https://www.youtube.com/@cuttingclockwork), a YouTube channel about practical AI workflows for video creators.

## Requirements

- A personal Google account (not a work or school account), 18 or older, with **Keep Activity** on. Skills don't need a paid subscription. They are rolling out gradually; if you don't see them yet, use the prompt fallback below.
- A finished video file, for example an MP4 exported from your editor.

## Install

### Upload it to Gemini

1. **Download** `SKILL.md` from the [latest release](https://github.com/cuttingclockwork/gemini-video-audit/releases/latest). It's a plain text file: open it and read it first, so you know exactly what Gemini will be told to do.
2. Open [gemini.google.com/skills](https://gemini.google.com/skills) (or in Gemini: **Settings → Skills**) and click the **Upload skill** button (the arrow icon).
3. Choose **files**, select `SKILL.md` and confirm.

Check the result: the skill is called `audit-short-form-video`, and its instructions end with the "Honesty rules" section.

**Updating:** delete the old skill and upload the new `SKILL.md`.

### Or create it manually

On the Skills page, click **Create manually**. Download `manual-setup.txt` from the [latest release](https://github.com/cuttingclockwork/gemini-video-audit/releases/latest). It contains three blocks (**Skill name**, **Description** and **Instructions**): copy each block into the field with the same name.

Asking Gemini to create the skill from a link to the file did not work in our test, so download the file and upload it.

### No skills yet?

Copy the **Instructions** block from `manual-setup.txt` into a new chat, attach your video, and add the level you want, for example "Level 2".

## Run your first audit

In a new Gemini chat, type `@`, pick `audit-short-form-video`, attach your video and send it. Add the level to your message ("Level 1") and Gemini starts right away. Without a level, it asks you once which level you want and then runs to the end. Within the same chat it keeps that level for your next videos; a new chat asks again.

**Customize your defaults (level, language, niche, platform):** open the skill on Gemini's Skills page and edit the four lines right at the top:
- `Default level: ask` → change `ask` to `1`, `2` or `3` so it never asks for the level.
- `Default language: video` → change `video` to for example `English` or `Nederlands` to always get the report in that language (alternative hooks and voice-over stay in the video's spoken language so you can use them directly).
- `Default niche: auto` → change `auto` to your niche, for example `DIY`, `beauty` or `SaaS`, so the audit judges your video against what works in that niche.
- `Default platform: auto` → change `auto` to for example `Instagram Reels`, `TikTok` or `YouTube Shorts`.

Gemini can also start the skill on its own when you upload a video and ask for feedback.

The report is written in the language spoken in your video (unless you set a default language or ask for another language in your message, such as "in English, please").

Each report includes one or two ideas marked **Experiment**: techniques your video doesn't use yet, worth testing but not proven fixes. Every report also ends its fixes with **How to tell if it worked**: the two or three numbers to check after publishing (such as how many viewers are still watching after 3 seconds, the average percentage viewed, rewatches, shares and saves), and how to compare them fairly with your own recent videos. That comparison is a hint, not proof: it's not a real A/B test.

You always get exactly three alternative hooks (at the Quick level: one better opening line).

## Limitations

- **Gemini samples frames and receives no file metadata.** It sees a selection of frames plus the audio, not every single frame or container metadata (exact resolution, frame rate, codec). Timecodes are to the second, not frame-accurate, and very short flash cuts or text pops can be missed. The skill tells Gemini to say so when it is unsure instead of guessing.
- **Sound levels are judged by ear, not measured.** Gemini checks voice clarity, music balance, volume consistency and clipping by ear. Any LUFS or dB values in the report (such as -14 LUFS or 12-18 dB ducking) are editing targets, not digital measurements.
- **No sound, no overall score.** If Gemini can't hear the audio, sound is marked N/A and there is no overall score.
- **Built for vertical short-form.** Horizontal or longer videos get a note, and only the criteria that make sense are applied.
- **Editorial rules of thumb.** The weights and timings are not calibrated against real performance data.
- **Privacy.** Your video is uploaded to Google. Check Gemini's privacy settings before uploading client or unreleased work.

## How this was built and tested

I'm a video creator, not a programmer: Claude (Anthropic's AI assistant) and Antigravity wrote and refined this skill. It contains no code that runs on your computer; it's instructions for Gemini. It was tested in the Gemini web app: uploading the file, the level question, the default lines, the report language and the full report (see the [changelog](CHANGELOG.md)). Provided as is, without warranty (see the license).

## Help

Something wrong or unclear? [Open an issue](https://github.com/cuttingclockwork/gemini-video-audit/issues).

## License

Free to use, also for paid client work, and free to change for your own use. Not for resale or redistribution: to share it, link to this page. See [LICENSE](LICENSE).

## Technical details

- `audit-short-form-video/SKILL.md` is the skill, in the open SKILL.md format: a header with `name` and `description`, followed by the instructions.
- The version number is the line right below the title in `SKILL.md`.
- `manual-setup.txt` in each release holds the same text as `SKILL.md`, split into the three fields of Gemini's **Create manually** form.
