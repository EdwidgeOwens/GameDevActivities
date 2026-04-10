# Simple Scene with a Moving Node (Godot 4)

## Project Overview

This activity demonstrates how to create a simple **3D scene in Godot 4** that displays a **“Hello World”** text and animates it as a **moving node**. The goal is to understand basic 3D scene setup, node hierarchy, and simple scripting using **GDScript**.

---

## Objectives

* Create a new 3D Godot project
* Add basic 3D scene components (camera and lighting)
* Display a “Hello World” text in 3D space
* Apply a script to make the text move smoothly
* Ensure the text behaves as a true 3D object

---

## Tools and Requirements

* **Godot Engine 4.x**
* Desktop/Laptop computer
* Basic knowledge of nodes and scenes

---

## Scene Structure

```
MainScene (Node3D)
├── Camera3D
├── DirectionalLight3D
└── HelloText (Label3D)
```

---

## Steps Performed

### 1. Create the Project

* A new Godot project named **“Simple Scene with a Moving Node”** was created using the default 3D renderer.

### 2. Create the Main Scene

* A **Node3D** was added as the root node and named `MainScene`.

### 3. Add Camera and Light

* A **Camera3D** was positioned in front of the scene and set as the current camera.
* A **DirectionalLight3D** was added to properly illuminate the 3D text.

### 4. Add Hello World Text

* A **Label3D** node named `HelloText` was added.
* The text property was set to:

  ```
  Hello World
  ```
* Billboard mode was **disabled** so the text behaves like a real 3D object.

### 5. Make the Text Move

* A GDScript was attached to `HelloText`.
* The script uses a sine function to move the text left and right smoothly over time.

### 6. Run the Scene

* The scene was saved as `MainScene.tscn` and set as the main scene.
* When run, the text moves continuously in 3D space.

---

## Result

The output is a simple 3D scene where the **“Hello World”** text moves smoothly from side to side, demonstrating basic 3D movement and scripting in Godot.

<img width="1142" height="643" alt="Screenshot 2026-01-31 at 5 43 08 PM" src="https://github.com/user-attachments/assets/63afacf4-e78e-4745-8c9e-d046a47c4f05" />

---

## Learning Outcome

Through this activity, the following concepts were learned:

* Creating and organizing 3D scenes in Godot
* Using Label3D for 3D text
* Understanding camera-facing vs true 3D objects
* Applying frame-based movement using `_process(delta)`

---

# 🎮 2D Platformer Game (Godot)

## 📌 Project Overview

This is a **2D platformer game built in Godot Engine**, developed as part of a structured learning progression covering gameplay mechanics, level design, UI/UX, and AI.

The game focuses on:

* Physics-based movement
* Hazard-based gameplay (instant death)
* Enemy interaction
* Level progression with increasing difficulty

---

## 🗂️ Project Structure

### 🎬 Scenes

```
game.tscn          # Main game scene
player.tscn        # Player character
slime.tscn         # Enemy (basic AI)
platform.tscn      # Platform objects
killzone.tscn      # Instant-death zones (spikes/traps)
coin.tscn          # Collectible item
music.tscn         # Audio / background music handler
```

### 🧠 Scripts

```
player.gd          # Player movement & controls
slime.gd           # Enemy AI behavior
coin.gd            # Coin logic (collection)
killzone.gd        # Death trigger logic
game_manager.gd    # Game state management (restart, level control)
```

---

## 🎮 Core Gameplay Mechanics

### 🕹️ Player Controller

Implemented in `player.gd`:

* Left / Right movement
* Jumping using physics
* Collision detection with:

  * Platforms
  * Enemies
  * Hazards

### ⚠️ Death System

* No HP system
* Player dies instantly when touching:

  * `killzone` (spikes/traps)
  * `slime` (enemy)
* Death triggers:

  * Scene reload or restart via `game_manager.gd`

---

## 👾 Enemies (AI)

### 🟢 Slime Enemy (`slime.tscn`)

* Basic movement behavior (likely patrol or directional)
* Acts as a **kill-on-contact entity**
* Controlled via `slime.gd`

---

## 💰 Collectibles

### 🪙 Coin System (`coin.tscn`)

* Player can collect coins
* Logic handled in `coin.gd`
* Can be extended to:

  * Score system
  * Unlockables

---

## 🧱 Level Design

### Features

* Tile/platform-based layout
* Hazard placement using `killzone.tscn`
* Progressive difficulty design

### Mechanics

* Instant restart on failure
* No checkpoints (hard reset gameplay loop)

---

## 🎵 Audio System

### `music.tscn`

* Handles background music playback
* Can be expanded using:

  * Audio buses
  * SFX layering (jump, death, coin pickup)

---

## 🧠 Game Management

### `game_manager.gd`

Responsible for:

* Restarting the level
* Managing game state
* Handling transitions (e.g., Level 1 → Level 2)

---

## 📚 Academic Mapping

### Week 2 – Gameplay Mechanics

✔ Input handling (movement, jump)
✔ Physics system (collision, gravity)
✔ Player controller implemented

### Week 2 – Level Design

✔ Platforms and hazards implemented
✔ Killzone system (instant death)
✔ Difficulty progression structure

### Week 3 – UI/UX & Audio

✔ Background music system (`music.tscn`)
✔ Foundation for UI integration

### Week 3 – AI & Enemies

✔ Enemy entity (`slime`)
✔ Basic AI behavior implemented

---

## ⚙️ How to Run

1. Open project in **Godot Engine**
2. Load:

   ```
   game.tscn
   ```
3. Press ▶ Run

---

## 🚀 Future Improvements

* Add:

  * HUD (score, lives, level indicator)
  * Level 2 notification system
* Improve enemy AI:

  * Patrol + chase behavior (FSM)
* Add animations:

  * Idle / Run / Jump / Death
* Implement sound effects:

  * Jump
  * Coin pickup
  * Death
* Add checkpoints instead of full restart (optional)

---

## 🧪 Design Philosophy

This project uses a **fail-fast gameplay loop**:

* Immediate feedback (death on mistake)
* Encourages precision and timing
* Simple mechanics, skill-based progression

---

## 📄 Notes

This project is developed for **educational purposes** under structured weekly activities.

---


## Author

**Clive Owen Delima**

---

## Notes

This project serves as a foundation for more advanced concepts such as user input, animations, and interaction with other 3D objects.
