# fun-projects

Personal project tracker apps by engrart.

## Structure

- `record-tracker/` — app to track a vinyl record collection (`index.html`)
- `pickeball-tracker/` — pickleball game tracker

## Conventions

- Vanilla HTML / CSS / JavaScript — no build tools, no frameworks
- Each app lives in its own directory with a single `index.html` entry point
- Keep everything self-contained in `index.html` (inline `<style>` and `<script>`) unless the feature is large enough to warrant separate files
- Use `localStorage` for persistence (no backend)
- Mobile-friendly layouts preferred

## When implementing an issue

- Read the existing `index.html` in the relevant tracker before making changes
- Match the existing visual style and JS patterns exactly
- Test that the page would load correctly in a browser (no syntax errors)
- Commit with `Fix #<number>: <title>`
