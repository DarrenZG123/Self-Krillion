# Self-Krillion
A Krillion-inspired trivia game where you write the prompts. Set a question, its one accepted answer, and a rarity tier, then dive: rarer answers sink your krill deeper into a pixel-art ocean.

## Play
Open `index.html` in any browser. No install or build step needed.

## How it works
1. Open the menu (☰) or **Edit prompts** and choose how many prompts (1–20) and how many seconds each gets (15, 25, 45 or no timer).
2. For each prompt, enter the question, the one accepted answer, and its rarity.
3. Press **Begin dive** and hand it to a player.

| Tier | Points | Sinks |
|---|---|---|
| Plankton | 10 | 100 m |
| Too Clever | 15 | 150 m |
| Schooler | 30 | 300 m |
| Rare | 60 | 600 m |
| Deep Cut | 85 | 850 m |
| One in a Krillion | 100 | 1,000 m |

- A close guess, like a small typo, is autocorrected. Press Dive again to confirm it.
- A wrong guess shakes the input with a "no echo" message.
- Running out of time scores 0 for that prompt.
- A perfect dive is every answer at One in a Krillion (100 × the number of prompts).

Prompts are saved in your browser's local storage.

## Tech
A single self-contained HTML/CSS/JavaScript file with no frameworks. Answers are matched with text normalization (case, accents, punctuation, a leading "the") plus Levenshtein edit distance (up to 20% of the answer's letters). The ocean, sprites and animations are drawn with inline SVG, CSS and a canvas.

Inspired by [Krillion](https://krillion.io). This is an unofficial fan project and is not affiliated with it.
