# sc-ohseearr-fixtures

Test frames for the readers of [sc-ohseearr](https://github.com/w00zla/sc-ohseearr): single frames of the
maintainer's own debug recordings of Star Citizen, each with the cursor the recording stored. sc-ohseearr's reader
tests read them through its submodule `fixtures/` and assert what the frames show (values checked by hand).

| Folder | Reader | Frames |
|---|---|---|
| `gear-inventory/` | the character inventory | 2 at 3840×1600, 4 at 1920×1080 |
| `refinery/` | the refinery terminal | 3 at 3840×1600, 4 at 1920×1080 |
| `warehouse/` | the warehouse (item bank) | 3 at 3840×1600, 4 at 1920×1080 |

Each folder's `NOTES.md` names the recording, the date and the game build of every frame. A frame is
`<recording id>-read-<n>.jpg` (JPEG q90, as the companion app recorded it) with `<recording id>-read-<n>.json`
(`{"cursor": [x, y]}`, in frame pixels, or `null`).

**Only small sets of single frames go here**, never whole recordings, screenshot folders or files extracted from the
game.

## Licence

The frames show game content. Star Citizen® is a registered trademark of Cloud Imperium Rights LLC; game content and
materials are copyright Cloud Imperium Rights LLC and Cloud Imperium Rights Ltd. This repository is an unofficial fan
project, not endorsed by or affiliated with the Cloud Imperium group of companies. The frames are kept for testing
sc-ohseearr only; no licence to them is granted.
