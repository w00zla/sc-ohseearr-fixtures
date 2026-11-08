# sc-ohseearr-fixtures

Test frames for the readers of [sc-ohseearr](https://github.com/w00zla/sc-ohseearr): single frames of Star Citizen
from debug recordings, each with the cursor position recorded with it. sc-ohseearr includes this repository as its
submodule `fixtures/`; the readers' tests read the frames and assert what they show.

## Layout

One folder per reader, named like the reader in sc-ohseearr's `readers/` (`gear-inventory/`, `refinery/`,
`warehouse/`). Each folder's `NOTES.md` lists its frames: recording, date, game build, resolution and what the frame
shows.

A frame is `<recording id>-read-<n>.jpg` (JPEG as recorded) with `<recording id>-read-<n>.json`: `{"cursor": [x, y]}`
in frame pixels, or `{"cursor": null}`.

## Adding frames

- Frames come from an app's debug recordings (what a reader gets live: the grab with its cursor), not from
  screenshots, and from your own play sessions.
- Single frames only: up to ~1 MB each, a few MB per reader. Never whole recordings, screenshot folders or files
  extracted from the game.
- Cut the recording's JSON down to the cursor: no paths, names or other personal data.
- Add a row per frame to the reader's `NOTES.md`. Every value a test asserts is checked by hand against the frame.
- Most useful: resolutions, screens and states a reader's frames do not cover yet.
- In sc-ohseearr, move the submodule to the new commit together with the tests that use the frames.

## Licence

The frames show game content. Star Citizen® is a registered trademark of Cloud Imperium Rights LLC; game content and
materials are copyright Cloud Imperium Rights LLC and Cloud Imperium Rights Ltd. This repository is an unofficial fan
project, not endorsed by or affiliated with the Cloud Imperium group of companies. The frames are kept for testing
sc-ohseearr only; no licence to them is granted.
