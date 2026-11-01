# PROCESS — Beat to Move
### SD5913 Assignment 3: An Interactive Experience

## 1. Initial Idea and Motivation

My initial idea was to create a small side-scrolling rhythm game in which a character automatically moves forward while players respond to music through jumping and obstacle avoidance.

As someone with a design background and limited programming experience, I wanted to explore how simple interactions could create an enjoyable and responsive experience.

I was particularly interested in the relationship between music, movement, and visual feedback.

My initial design question was:

**How can musical rhythm influence player movement and turn simple obstacle avoidance into an engaging interactive experience?**

Rather than developing a complex game with multiple systems, I began with one fundamental interaction: pressing Space at the right moment to jump over an obstacle.

## 2. Concept Exploration

During the concept development stage, I explored two main directions:

**Concept A — Beat Runner**

A side-scrolling game where players synchronize jumps with musical beats to avoid obstacles.

**Concept B — Build the Beat**

A rhythm-based experience where correctly timed actions generate platforms and modify the environment.

After considering gameplay clarity, technical difficulty, and the available development time, I selected Concept A as the core interaction.

I also retained one idea from Concept B: player actions could influence the visual environment and create a stronger sense of musical immersion.

This led to the final direction:

**Beat to Move — a rhythm-based runner with reactive visual feedback.**

## 3. Development Process and Iterations

### Iteration 1 — Basic Character Movement

I started with a simple HTML Canvas environment containing a running character, a scrolling city background, and moving ground elements.

The character remained in a fixed horizontal position while the environment moved, creating the illusion of continuous forward movement.

This established the basic visual structure of the game.

### Iteration 2 — Jump Interaction

I introduced keyboard input using the Space key.

The character's vertical movement was calculated using jump velocity and gravity, allowing the character to jump and land naturally.

I also prevented repeated jumping while the character was airborne.

This changed the project from a passive animation into an interactive experience.

### Iteration 3 — Obstacle Avoidance

I introduced triangular obstacles and a simplified collision detection system.

Obstacles moved towards the player, who could jump to avoid them.

The game displayed immediate feedback through "HIT" and "CLEARED" messages.

This was the first functional gameplay loop involving player input, system response, and feedback.

### Iteration 4 — Rhythm and Timing Judgment

The next challenge was connecting jumping to music.

Initially, players could jump at any time, making the experience closer to a traditional running game.

I introduced a fixed 80 BPM rhythm and timing judgment windows.

Player inputs were categorized as Perfect, Good, or Miss.

Each obstacle was also limited to one input attempt to discourage random key pressing.

This made timing an important condition for successful gameplay.

### Iteration 5 — Scoring and Replay

I added a scoring system, a completion state, and a Play Again function.

Players could finish a complete run, review their performance, and retry.

I deliberately retained a translucent results overlay because it allowed the background environment to remain partially visible, maintaining continuity between gameplay and the final result.

### Iteration 6 — Visual and Interaction Redesign

After reviewing the initial prototype, I felt that the visual presentation was too basic.

The original interface contained large amounts of text inside a relatively small gameplay area. The environment also lacked a distinctive visual identity.

I therefore redesigned the interface using a retro neon-city direction, enlarged the game canvas, and reorganized the score display into a more compact HUD.

I also expanded the interaction beyond jumping by introducing Shift-based sliding.

This created different obstacle responses and made the gameplay less repetitive.

### Iteration 7 — From Metronome to Music

One of the most important changes was replacing the original metronome-like sounds.

Although the first version had rhythm detection, the repeated electronic beeps did not provide the experience I expected from a music game.

With AI assistance, I created an original electronic instrumental track, **Night Drive**, with melodic synthesizers, harmonic layers, bass, and percussion.

I then redesigned the obstacle sequence to follow the musical timeline, introducing 22 obstacle events, consecutive jumps, and short and long slide sections.

I also changed the ending behavior. Instead of immediately interrupting the soundtrack when the final obstacle passed, the game now allows the musical outro to finish before displaying the results.

## 4. Challenges and Problem Solving

### Challenge 1 — Programming Structure

While modifying the keyboard interaction, I accidentally removed part of the animation function and misplaced a closing brace.

This caused the character and movement animation to disappear.

By checking the program structure and debugging the JavaScript code with ChatGPT, I restored the draw function and corrected the obstacle loop.

This helped me better understand how JavaScript functions, loops, and animation updates depend on each other.

### Challenge 2 — Gameplay Repetition

The early prototype included eight equally spaced triangular obstacles.

Although the collision and scoring systems worked, the predictable obstacle sequence made gameplay repetitive.

I expanded the game to include two primary actions, multiple obstacle configurations, and musical phrases containing combinations of jumps and slides.

### Challenge 3 — Music Synchronization

The early rhythm system used synthesized beats rather than a complete musical composition.

In the later version, the original soundtrack became the reference timeline for obstacle positioning and timing judgments.

This reduced the risk of music and gameplay drifting apart.

### Challenge 4 — Scope Management

I considered allowing users to upload their own music and automatically generate obstacle maps.

However, accurately extracting beats, interpreting musical structure, and generating appropriate obstacles would require a more advanced system and additional testing.

I therefore chose a fixed original soundtrack to prioritize a functional interactive experience within the assignment deadline.

## 5. Design Review Findings

Reviewing the current prototype revealed three areas for further development:

**1. Greater Obstacle Variety and More Complex Rhythms**

The game could benefit from more obstacles, alternative movement requirements, and less predictable rhythmic combinations, such as three consecutive jumps followed by a slide.

**2. Stronger Visual Contrast for Obstacles**

Although obstacles use distinctive colors, stronger glow effects, outlines, or animation could help them stand out more clearly against the city background.

**3. Multiple Levels and Progressive Difficulty**

The current game contains one musical level. Adding several levels with different soundtracks, speeds, and obstacle patterns would create a stronger sense of progression and replayability.

These points are proposed improvements rather than completed features.

## 6. Actual User Trial

Tester: Friend Zheng Jingyi

Test procedure: The participant was invited to try Beat to Move with minimal instructions. They were asked to explore the game independently, use the keyboard controls, and complete a full run. After playing, they were encouraged to share their thoughts on the gameplay, obstacle design, visual clarity, and overall experience.

Observed Behavior: The participant was able to start the game and understand the basic jumping and sliding controls without significant difficulty. The gameplay ran smoothly, and the participant was able to respond to different obstacles and understand the scoring feedback. No major technical or usability issues were identified during the session.

Feedback:
1. More Obstacle Variety and Rhythmic Challenges
The participant suggested introducing more obstacles, additional avoidance mechanics, and more varied rhythmic patterns. More challenging combinations, such as three consecutive jumps followed by a slide, could make the gameplay less repetitive and more engaging.

2. Stronger Visual Highlighting of Obstacles
The participant suggested adding glowing outlines or lighting effects to the obstacles to make them stand out more clearly from the background, especially during fast-paced gameplay.

3. Multiple Levels
The participant suggested adding more levels with different soundtracks, obstacle arrangements, and increasing difficulty to improve replayability and provide a stronger sense of progression.

Design response:1. Partially Implemented — Obstacle Variety

During development, I expanded the original eight triangular obstacles into 22 obstacle events, introducing short slides, long slides, and consecutive jumping sequences. These changes made the gameplay more varied. Additional obstacle mechanics and more complex rhythmic combinations remain potential future improvements.

2. Partially Implemented — Visual Clarity

I redesigned the original environment using a neon-inspired visual style and contrasting colors to distinguish obstacle types. I decided to retain the existing background and translucent results screen to maintain visual continuity. Stronger glowing outlines and animated obstacle highlights are planned for future refinement.

3. Deferred — Multiple Levels

I decided to prioritize one complete and functional musical level rather than developing several unfinished levels within the assignment deadline. Multiple levels with different music tracks, difficulty settings, and obstacle patterns will be considered in future development.

Reflection: The feedback helped me identify opportunities to improve gameplay variety, visual clarity, and replayability. While some improvements were incorporated into the current prototype, others were deliberately deferred to maintain a manageable project scope. This reinforced the importance of balancing creative ambitions, technical feasibility, and user experience in interactive design.

## 7. AI Use and Critical Decisions

I used ChatGPT as a design discussion partner and coding assistant throughout this assignment.

Its contributions included:

- Comparing interaction concepts and evaluating technical feasibility.
- Explaining basic HTML Canvas and JavaScript programming.
- Assisting with keyboard input, jumping, collision detection, timing judgments, and scoring.
- Debugging syntax and animation problems.
- Supporting UI redesign and original soundtrack generation.
- Helping structure and edit project documentation.

I tested the program in my own browser and made decisions about which ideas to retain or reject.

**Suggestion Accepted:** I adopted the recommendation to focus on a simple rhythm runner before introducing additional movement mechanics. This allowed me to establish a working interaction loop before extending the game.

**Suggestion Modified:** I initially considered keeping the project as a minimal single-action rhythm game, but decided that repetitive beeps and equally spaced obstacles were not engaging enough. I expanded the interaction to include musical phrases, sliding, and an original soundtrack.

**Suggestion Rejected or Deferred:** I decided not to implement automatic level generation from arbitrary user-uploaded songs because it was outside the reliable scope of this assignment.

AI-generated code and design suggestions were treated as starting points that required testing, debugging, and design evaluation rather than as automatically correct solutions.

## 8. Reflection and Future Development

This project helped me understand the difference between creating an animation and designing an interactive experience.

The most significant learning outcome was realizing that player input must meaningfully affect the system and produce understandable feedback.

I also learned that a technically functioning mechanism does not necessarily create an engaging experience. Music quality, timing, visual hierarchy, obstacle variation, and responsiveness all influence how players perceive the interaction.

If I continue developing Beat to Move, my priorities would be:

1. More expressive obstacle visuals and timing feedback.
2. Additional movement variations and rhythmic patterns.
3. Multiple levels with progressive difficulty.
4. Improved onboarding and accessibility.
5. Optional music selection and more advanced music analysis.

Ultimately, Beat to Move represents my exploration of how programming, music, and visual design can work together to transform simple keyboard actions into an interactive experience.

## 9. Credits

The project was developed as an individual SD5913 assignment with ChatGPT assistance.

The soundtrack `nightdrive-original.ogg` was created for this project using AI-assisted algorithmic synthesis.

No commercial recordings or copyrighted songs were embedded.

The development history is documented through the Git repository commits.
