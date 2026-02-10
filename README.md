# song-to-lyrics-with-timecode

**song-to-lyrics-with-timecode** is an experimental project that converts songs into time-synchronized lyrics using OpenAI’s Whisper (Tiny model).

The project focuses on extracting **word-level timestamps** and aligning them with audio playback.
It is currently **a work in progress**.

---

## Project Goal

The goal is to generate lyrics with accurate timecodes that can be:

* displayed in sync with the music,
* used for karaoke-style interfaces,
* or explored for fine-grained audio–text alignment.

This project was initially built around one of my favorite songs.

---

## Current Features

* Audio transcription using **Whisper Tiny**
* Word-level timestamps
* Chunked transcription for long audio files
* Basic merging of words into readable segments
* Synchronous playback of audio segments

---

## Main Challenge

The hardest part of this project is **synchronization**:

* aligning Whisper timestamps with real audio playback,
* handling gaps and overlaps between words,
* merging words into meaningful lyric segments without breaking timing.

This problem is still being actively worked on.

---

## How It Works (Current Pipeline)

1. Load audio file
2. Transcribe using Whisper Tiny with word timestamps
3. Merge close timestamps into lyric segments
4. Print and play each segment in sync with the audio

---

## Example Output

```
[12.30 - 14.10]: Let me down slowly
[14.20 - 16.05]: If you let me down slowly
```

---

## Limitations (Work in Progress)

* Timing is not yet perfectly stable
* Playback synchronization can drift
* No GUI or karaoke-style display
* No automatic lyric line segmentation
* Currently tested on a single song

---

## Planned Improvements

* More robust timestamp alignment
* Smarter lyric segmentation
* Non-blocking audio playback
* GUI or terminal-based lyric display
* Support for multiple songs and formats

---

## Dependencies

```bash
pip install torch transformers pydub numpy
```

A compatible audio backend is required for playback.

---

## Status

🚧 **Work in progress**
The project is experimental and not yet finalized.

---

## Contributing

Ideas, feedback, and contributions are welcome, especially around:

* audio/text synchronization,
* timestamp alignment,
* playback handling.
* Even if it's just to upload a new song (btw i love beautiful and meaningfull song).
