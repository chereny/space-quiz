# Copilot instructions

## Project structure and architecture

This repository is a dependency-free static page. `index.html` contains the document, all styling, the quiz content, and the application logic; there is no separate build or application layer.

The quiz is data-driven: the `questions` array holds question text, answer options, the correct option index, and the explanatory fact. `renderQuestion()` creates the answer buttons for the current item, while `selectAnswer()` records the choice, updates score/progress, and shows feedback. `showResults()` presents the completion summary; the restart handler resets state and renders the first question. Keep changes to quiz content in the data array and preserve this flow when changing quiz behavior.

## Commands and verification

There are no package manifest, build, lint, or test-runner files in the repository, so no project-defined build, lint, or automated test commands are available. To check the quiz, open `index.html` directly in a browser and exercise answer selection, next-question navigation, results, restart, and the 1–4 keyboard shortcuts. Check both light and dark color schemes and reduced-motion behavior when changing styles.

## Code conventions

- Keep the page self-contained in `index.html`; there are currently no external libraries or assets.
- Use the existing CSS custom properties for colors and surfaces, including their dark-mode overrides. Honor the existing small-screen and reduced-motion media queries.
- Build answer options as DOM elements and insert quiz-provided text with `textContent` or text nodes rather than treating it as HTML.
- Preserve accessible interaction patterns: semantic buttons, the question/answer group labels, live score and feedback, progress-bar values, visible keyboard focus, keyboard shortcuts, and focus movement after answering and when changing questions or showing results.
- Keep quiz state in `current`, `score`, and `answered`, and update the DOM through the existing render, answer-selection, and results functions so the displayed progress and score remain consistent.
