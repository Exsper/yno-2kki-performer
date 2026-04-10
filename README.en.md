# YNOproject Yume2kki Performer

Automatically plays music based on a given score.

## Before using this script, please ensure that the key assignment in the game is type A (press Shift+Z+X+→ in piano window to set if not)

## How It Works

The script uses the touch‑screen key simulation method provided by the original webpage (`simulateKeyboardInput`) to simulate keyboard input and play specified notes.

This script does not modify any original webpage functions, game content, or saved data.

Although it can simulate keyboard input, its functionality is limited to playing notes; it does **not** provide automatic movement or exploration assistance. If the character moves on its own while the script is running, it is likely because the piano window is not open.

## Score Formats

### Standard Notation

- Each note lasts for a quarter note (1/4 beat).
- Pitch range: C3 ~ C5.
- `0` indicates a rest.

Example score:

```text
G4 0 0 0 0 0 G4 0 A#4 0 G#4 G4 0 F4 0 0 D#4 0 0 0 0 0 D#4 0 F4 0 0 C4 0 0 D4 0 G3 0 0 0
（All spaces can be deleted）

BPM: 240
```

### JE Score

See [JE Score](https://madderscientist.github.io/je_score_operator/) for details.

Example score:

```text
2   (6)23 #4   6  33   #4  23   #4   2   (6)23 #4   6  33   #43  #4   

BPM: 300
```

```text
5 4 5 1 2 4 5 4
5 1 2 4 5 4 5 1
2 4 #6 6 4 1 2 4
5 4 5 1 2 4 5 4 0

BPM: 257
```

### MIDI

Due to limitations of single‑key input and pitch range, only MIDI files that meet specific requirements can be played successfully.

## Pitch adjustment

You can adjust the overall pitch of JE Score and MIDI. Fill in the number to represent how many semitones to move, which must be an integer (positive number indicates pitch up).
