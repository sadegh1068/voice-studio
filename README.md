# Voice Studio

A single-page recorder for building a personal text-to-speech fine-tuning set on a phone or tablet.
It shows one sentence at a time, records it in the browser as 48 kHz 16-bit WAV (echo cancellation,
noise suppression and auto-gain off), checks each take for clipping, level, room noise and length, keeps
the takes in the browser's storage, and exports a ZIP of `clips/*.wav` plus `manifest.jsonl`.

Each line also carries reading direction: a pace with a target words-per-minute range, an emotion and a
one-line delivery note. After every take the page measures the speaking pace (words divided by the time from
the first to the last sound), looks for a mouth click or tap after the last word, and offers to re-record or
keep the take. A menu filters and orders the lines (to do, paragraphs, recorded, needs a look; by emotion or pace).
The export manifest includes the direction and the measurements.

An optional examples pack (a ZIP made offline, not part of this repository) can be imported from the menu; it
adds an Example button that plays a reference reading of each line. It is stored in the browser only.

Nothing is uploaded: recordings stay on the device until you export them.

Open the page over https, tap Start, allow the microphone. The page also works offline after the first
visit (service worker).
