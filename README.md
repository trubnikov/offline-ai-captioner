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



## Limitations & Future Improvements

**Limitations**
- Subtitle timing resets: Each message or phrase starts timecodes from 00:00. This means time does not accumulate across the whole conversation. For most offline and accessibility use cases, this is sufficient, but for real-time video or long dialogue, cumulative timing may be useful.
- No true audio synchronization: The subtitles are generated from text or dictation input. Automatic detection of exact speech timing and pauses is not implemented (but can be added with tools like Whisper or integrated macOS transcription).
- Manual splitting: For best results, each phrase should be sent as a separate input. Full text paragraphs may result in less precise subtitle splitting.

**Future Improvements & Extensions**
- Multi-language support: Add an optional translation feature (e.g., English ↔ Spanish or any other target language), allowing real-time subtitles for multilingual meetings.
- SRT/VTT export: Allow exporting generated subtitles to popular formats like .srt or .vtt for direct use in video editing and publishing.
- Automatic time alignment: Integrate with speech-to-text models (like Whisper or built-in macOS tools) to provide accurate subtitle timing and phrase detection.
- Speaker identification: Optionally label subtitles with speaker names or roles for group conversations.
- Batch processing: Enable processing of full recorded meetings, podcasts, or lectures as a single file.
