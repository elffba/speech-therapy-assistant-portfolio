# speech-therapy-assistant

> Turkish articulation disorder detection — phoneme-level scoring on mobile.

A mobile app that records speech and shows exactly which sounds a user struggles with.  
Built as my graduation project at Dokuz Eylül University.

To my knowledge, **the first articulation analysis tool built specifically for Turkish.**

---

## the core problem

Most speech-to-text models normalize mispronunciations.  
Whisper transcribes `"şşşeker"` as `"şeker"` — useless for therapy.

So I used `wav2vec2-xls-r` (Turkish fine-tuned, CTC-based) with Viterbi forced alignment  
to get frame-level phoneme confidence scores instead of corrected text.

---

## stack

**Backend** — Python, FastAPI, wav2vec2 XLS-R, librosa, SQLite  
**Frontend** — React Native (Expo)
