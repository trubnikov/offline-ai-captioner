# Offline AI Captioner (Gemma 3n Accessibility Subtitler)

> Turn any spoken or written text into clean subtitles — 100% offline, for accessibility, privacy and instant use.

## What it does

- Converts any dictated or written text into readable subtitles (one line per phrase), each with a timing code.
- Works with any language.
- 100% offline — all processing happens on your Mac.

## How it works (step-by-step)

1. **Install [LM Studio](https://lmstudio.ai) on your Mac.**
2. **Download and load Gemma 3n model** (E4B or 12B) in LM Studio.
3. **Enable Dictation** (Settings > Keyboard > Dictation) on your Mac (optional, for voice input).
4. **Open LM Studio, create a new chat.**
5. **Paste the System Prompt** (see below) as the first message.
6. **Dictate or paste any text** — model will output subtitles.

## System Prompt
Format any input as subtitles for accessibility.
Instructions:
- Split the input text into sentences or logical phrases.
- For each line, add a time code, incrementing by 1 second for each phrase: 00:00, 00:01, 00:02, etc.
- Output only the subtitles. Do not translate, do not explain, do not add extra text.

Example:

Input:
Hello! How are you? Nice to meet you.

Output:
00:00 - Hello!
00:01 - How are you?
00:02 - Nice to meet you.

--

Begin.
