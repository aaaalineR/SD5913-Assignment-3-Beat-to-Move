# SD5913-Assignment-3-Beat-to-Move
# BEAT TO MOVE
### A Rhythm-Based Side-Scrolling Music Game

**SD5913 — Assignment 3: An Interactive Experience**

## 1. Project Overview

**Beat to Move** is a browser-based interactive music game that combines rhythm, character movement, and obstacle avoidance in a neon-inspired city environment.

The project explores how music can become an essential part of gameplay rather than simply functioning as background audio. Players must coordinate their actions with musical timing to overcome obstacles, maintain their rhythm, and achieve a higher score.

The experience is designed for casual players who enjoy short rhythm games and accessible keyboard-based interactions. No previous gaming experience is required.

## 2. Concept and Design Intention

The central concept is **"Move with the Music."**

Instead of allowing players to jump or slide successfully at any moment, the game connects player input to specific musical cues.

The player automatically travels through a side-scrolling city, while obstacles are arranged along a predefined musical timeline. By listening to the soundtrack and responding at the appropriate moments, players can overcome different challenges.

The experience follows a continuous interaction loop:

**Listen → React → Receive Feedback → Adjust → Continue**

The goal is to transform rhythmic listening into an active, physical-feeling experience through simple keyboard interactions.

## 3. Gameplay and Controls

The game currently contains one playable musical level with 22 obstacle events and an original electronic soundtrack lasting approximately 61.5 seconds.

### Controls

| Key | Action |
|---|---|
| Space | Jump over pink spikes |
| Shift (hold) | Slide under cyan gates |
| START RUN | Begin the game and soundtrack |
| SOUND ON/OFF | Mute or unmute audio |
| PLAY AGAIN | Restart after completing the level |

### Obstacle Types

- **Spikes:** Require a correctly timed jump.
- **Short Gates:** Require a correctly timed slide.
- **Long Gates:** Require players to hold Shift for a longer duration.

The obstacle sequence includes rhythmic combinations such as consecutive jumps followed by sliding actions.

### Scoring System

Player input is evaluated against a target timing window.

- **Perfect:** Accurate timing, 100 points.
- **Good:** Slight timing deviation, 50 points.
- **Miss:** Incorrect timing or unsuccessful obstacle avoidance, 0 points.

Each obstacle allows one input attempt. This discourages random key pressing and encourages players to respond deliberately to musical cues.

After the final obstacle, the soundtrack continues through its outro before displaying the results screen.

## 4. Visual and Audio Design

The visual direction is inspired by retro electronic music aesthetics and nighttime urban environments.

The game uses a dark color palette, neon pink and cyan obstacle indicators, a scrolling cityscape, and a compact heads-up display.

The visual feedback includes obstacle colors, character movement, timing judgments, scores, and a final results overlay. The results screen retains a translucent background to preserve a visual connection with the completed run.

### Original Soundtrack — Night Drive

The game includes an original electronic instrumental soundtrack created for this project with AI-assisted algorithmic synthesis.

It combines melodic synthesizers, harmonic layers, bass, and percussion to establish a consistent musical atmosphere.

The obstacle arrangement follows predetermined musical cues in this composition.

No commercial recordings, lyrics, or melodies from *Blinding Lights* or other copyrighted songs are included.

## 5. Technology

The project was developed using:

- **HTML5:** Page structure and interface.
- **CSS3:** Layout, typography, and visual styling.
- **JavaScript:** Player input, movement, collision detection, timing judgment, scoring, and game state.
- **Canvas 2D:** Character, environment, obstacles, and animation.
- **HTML Audio:** Soundtrack playback and timing synchronization.
- **GitHub:** Version control and development documentation.

The game uses native browser technologies without requiring a game engine or external JavaScript framework.

## 6. How to Run

1. Download or clone this repository.
2. Keep `index.html` and `nightdrive-original.ogg` in the same folder.
3. Open the project folder in Visual Studio Code.
4. Open a terminal in the project directory.
5. Run:

```bash
uv run --no-project python -m http.server 8000
```

6. Open `http://localhost:8000` in a desktop browser.
7. Click **START RUN** and play using Space and Shift.

The game is intended for desktop browsers with a physical keyboard. Chrome or Edge is recommended.

## 7. Known Limitations and Future Improvements

This project is a small interactive prototype rather than a full commercial rhythm game.

Current limitations include:

- Only one playable musical level.
- A fixed original soundtrack rather than user-uploaded music.
- A limited range of obstacle types and rhythmic patterns.
- Keyboard-focused interaction rather than mobile touch controls.
- Simplified collision detection and fixed timing windows.

Potential future developments include more complex obstacle sequences, brighter obstacle highlights, multiple levels with different difficulties, improved slide animations, and an optional user-provided music mode.

Automatically generating levels from uploaded songs would require additional audio analysis and synchronization testing.

## 8. Credits and AI Acknowledgment

**Concept and design direction:** Student project for SD5913.

**Programming and development:** Developed through iterative prototyping with ChatGPT assistance.

**AI assistance:** ChatGPT was used for concept exploration, feasibility evaluation, JavaScript development, debugging, visual refinement, soundtrack generation, and documentation support.

**Music:** `nightdrive-original.ogg` is an original algorithmically synthesized instrumental created for this project with AI assistance.

The project does not include third-party commercial music or external copyrighted visual assets.

Development changes are documented through the Git commit history and `PROCESS.md`.