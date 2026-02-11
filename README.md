# Broke-Budget Autopilot Content Agent

This repository contains a practical, no-code workflow to publish **English → Hindi → Odia** short tutorial videos using mostly free tools.

## Goal

Build a content pipeline that is:

- mostly free (`₹0–₹1,000/month`)
- phone + browser friendly
- semi-automatic now, near-autopilot later

---

## Architecture (Free Stack)

```text
Google Sheets   → Content Brain
ChatGPT         → Script Agent
TTS Tool        → Voice Agent
D-ID            → Avatar Agent
CapCut          → Caption Agent
YouTube + Meta  → Posting Agent
Make.com        → Automation Glue
```

---

## Phase 1 — Content Brain (Google Sheets)

Create a Google Sheet named **Word Video Engine** with the columns below:

| Column | Field |
|---|---|
| A | Word |
| B | Category |
| C | Script |
| D | Voice Text |
| E | Audio File Link |
| F | Video File Link |
| G | Title |
| H | Description |
| I | Status |

Add 50–100 starter words (examples: `Resilient`, `Negotiate`, `Reliable`, `Efficient`, `Grateful`).

---

## Phase 2 — Script Agent (Make.com + ChatGPT)

### Make.com Scenario

1. **Trigger:** `Google Sheets → Watch new rows`
2. **Action:** `OpenAI/ChatGPT → Create completion`
3. **Store output:** Save generated script in column **C (Script)**.

### Prompt Template

```text
Create a 40-second teaching video script.

Word: {{Word}}

Include:
Hook line
Simple English meaning
Hindi meaning
Odia meaning
2 short example sentences
CTA line

Subtitle-ready format.
Keep under 110 words.
```

---

## Phase 3 — Voice Agent (Free TTS)

Start with any free tier:

- ElevenLabs
- PlayHT
- Narakeet
- TTSMP3
- Clipchamp TTS

### Low-cost workflow

In Make.com, add a step to email yourself each generated script.

Then per video:

1. Copy script from email/sheet.
2. Paste in TTS tool.
3. Download MP3.
4. Upload MP3 to Google Drive.
5. Paste link in **E (Audio File Link)**.

---

## Phase 4 — Avatar Agent (D-ID)

Use `studio.d-id.com` free credits:

1. Choose avatar.
2. Upload MP3.
3. Paste script.
4. Generate video.
5. Download MP4.
6. Upload MP4 to Google Drive.
7. Paste link in **F (Video File Link)**.

---

## Phase 5 — Captions + Brand Template (CapCut)

Create one reusable template containing:

- word title animation
- Hindi line style
- Odia line style
- CTA banner
- low-volume background music

Per new video:

1. Open template.
2. Replace source avatar clip.
3. Export.

---

## Phase 6 — Posting Agent (Free Scheduling)

### YouTube Shorts

Use YouTube Studio scheduling:

- Upload 7 videos together.
- Schedule daily publishing.

### Instagram + Facebook

Use Meta Business Suite:

- Schedule both Instagram and Facebook posts for free.

---

## Phase 7 — Weekly Autopilot Loop (≈1 hour/week)

1. Generate 20 scripts.
2. Generate 20 voice files.
3. Generate 20 avatar videos.
4. Batch apply CapCut template.
5. Schedule uploads in YouTube + Meta.

---

## Phase 8 — Human-in-the-Loop Agent (Make.com)

Create a daily 9 AM scenario:

1. Pick one unused word from Sheet.
2. Send word to ChatGPT.
3. Save script to Sheet.
4. Email yourself script reminder.
5. Mark row as `READY` in **I (Status)**.

This creates practical near-autopilot with minimal manual effort.

---

## Title Template (Copy/Paste)

```text
Daily Useful English Word — {{Word}} | Hindi + Odia | 1-Minute Learning
```

## Description Template (Copy/Paste)

```text
Learn one powerful English word daily with Hindi and Odia meanings.

Save & share.

#englishlearning #odia #hindi #vocabulary
```
