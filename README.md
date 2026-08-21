# Flappy Bird Clone (Unity 2D)

A 2D Flappy Bird clone built in Unity as part of a game developer interview assignment. The player controls a bird that must fly through gaps between moving pipes without colliding with them.

## Features

- Space-bar flap control with Rigidbody2D-based physics
- Procedurally spawned pipes with randomized gap height
- Trigger-based scoring when the bird passes through a pipe gap
- **Dynamic difficulty**: pipe movement speed gradually increases as the player's score goes up, capped at a maximum speed
- Bird tilts up/down based on vertical velocity for a more natural flight feel
- Game over screen with a "Play Again" button that reloads the scene
- Continuous collision detection to prevent the bird from tunneling through fast-moving pipes at high speed

## How to Run

1. Clone this repository.
2. Open **Unity Hub** and add the cloned folder as a project.
3. Project was built using **Unity 6 (6000.5.9f1)** — using the same or a newer 6.x version is recommended.
4. Open the `SampleScene` scene inside `Assets/Scenes`.
5. Press **Play** in the Unity Editor.

## Controls

- **Space** — flap / fly upward
- Click **Play Again** on the Game Over screen to restart

## Project Structure

```
Assets/
  BirdScript.cs         - Player (bird) movement, flap input, collision/death logic
  LogicScript.cs         - Score tracking, difficulty scaling, game over/restart logic
  PipeMoveScript.cs       - Moves each pipe leftward, speed driven by LogicScript
  PipeMiddleScript.cs     - Trigger zone between pipes that awards score
  PipwSpawnerScript.cs   - Spawns new pipes at a set interval with randomized height
```

## Known Issues / Possible Improvements

- No sound effects or background music yet
- No mobile/touch input support (keyboard only)
- Difficulty curve (speed increase rate) could be exposed via a difficulty settings menu
- No high-score persistence between sessions (e.g. via PlayerPrefs)
- Pipe art/animation could be polished further

## Tech

- Engine: Unity 6 (6000.5.9f1)
- Language: C#
- Physics: Unity 2D physics (Rigidbody2D, Collider2D triggers)
