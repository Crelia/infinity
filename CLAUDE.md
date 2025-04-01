# CLAUDE.md - Assistant Guidelines

## Project Commands
- Run local server: `python -m http.server` (serves on localhost:8000)
- Validate HTML: `html-validate simtheory.html`
- Lint JS: `npx eslint simtheory.html --fix`
- Test audio: `ffmpeg -i Audio/*.mp3 -f null -`

## Code Style Guidelines
- HTML: Semantic tags, 2-space indentation
- CSS: Group related properties, use rgba for colors with opacity
- JavaScript:
  - Use const/let (not var)
  - camelCase for variables/functions
  - Group related functions (visual, audio, etc.)
  - Add comments for function blocks (like "=== AUDIO SYSTEM ===")
  - Keep functions focused and small (< 20 lines)
  - Use template literals for string interpolation

## Audio Implementation
- Use Web Audio API for all sound processing
- Initialize audio context on user interaction
- Handle browser compatibility issues (AudioContext vs webkitAudioContext)
- Keep drone volume low (0.15) with dynamic adjustments based on user interaction

## Animation Techniques
- Use requestAnimationFrame with setTimeout for controlled frame rate
- Implement fade effects with partially transparent black rectangles
- Use HSL color model for easier manipulation of hues