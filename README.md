# Voice Studio

A single-page recorder for building a personal text-to-speech fine-tuning set on a phone or tablet.
It shows one sentence at a time, records it in the browser as 48 kHz 16-bit WAV (echo cancellation,
noise suppression and auto-gain off), checks each take for clipping, level, room noise and length, keeps
the takes in the browser's storage, and exports a ZIP of `clips/*.wav` plus `manifest.jsonl`.

Nothing is uploaded: recordings stay on the device until you export them.

Open the page over https, tap Start, allow the microphone. The page also works offline after the first
visit (service worker).
