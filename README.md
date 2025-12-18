# Kahera 
**A 3D Horror-Simulation Game built with Unity & C#**

## About The Game
**Kahera** (The Cashier) is a first-person psychological horror simulation designed for mobile platforms. The player takes on the role of a night-shift cashier who must manage store duties while surviving a stalking entity. 

Unlike standard jump-scare games, Kahera relies on atmosphere, physics-based interactions, and an unpredictable AI that learns the map layout.

## Key Technical Features

### State-Machine AI System
The enemy utilizes a custom-built Finite State Machine (FSM) to switch between behaviors dynamically:
* **Patrol State:** Randomly navigates waypoints in the store.
* **Chase State:** Uses **NavMesh** pathfinding to pursue the player upon Line-of-Sight detection.
* **Search State:** Investigates the last known player location if line-of-sight is broken.
* *Code Reference:* `AI.cs`

### Modular Interaction System (Physics Raycasting)
Players can interact with the environment realistically. Instead of simple "press E to open" animations, I implemented physics-based manipulation:
* **Doors:** Weight and hinge physics applied via Rigidbody calculations.
* *Code Reference:* `DoorInteraction.cs`

### Mobile Optimization
Optimized for high-performance on mobile devices without sacrificing visual fidelity:
* **Custom Input System:** Implemented virtual joysticks and touch-sensitivity scaling.
* **Data Persistence:** Uses `PlayerPrefs` to save sensitivity settings and audio preferences locally.
* *Code Reference:* `MobilePlayerMovement.cs`, `SettingsManager.cs`

### Atmospheric Procedural Effects
* **Perlin Noise Lighting:** Implemented mathematical noise algorithms to create organic, non-repetitive flickering light effects for horror ambience (`FlickeringLight.cs`).
* **Dynamic Audio Triggers:** Sound effects triggered by physics collisions (e.g., falling boxes) to alert the AI (`FallingBox.cs`).

## Tech Stack
* **Engine:** Unity 6 (6000.2.8f1)
* **Language:** C#
* **3D Modeling:** Blender
* **Animation:** Mixamo
* **Version Control:** Git & GitHub

## How to Play (Developer Build)
1.  Just Download the apk file in the repository.

## Credits & Collaboration
This project was built as a collaborative effort by:
* **Lester Jude Garingalo** - Lead Programmer (AI, Core Systems, UI)
* **Cornelius James Lasala** - [Character Design, Documentation, 3D Assets]
* **Giann Villarosa** - [Documentation, Story]

---
*Note: This repository serves as a portfolio showcase. Some assets have been excluded for licensing reasons.*
