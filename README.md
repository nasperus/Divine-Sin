# Divine-Sin

**Divine-Sin** is a fast-paced, Hades-style roguelike built in Unity.  
You fight through procedurally linked rooms, defeat enemies and bosses, and choose between **abilities** or **stat upgrades** after each clear to shape your build on every run.

https://github.com/nasperus

---

## 🎮 Core Features

- **Hades-style roguelike loop** – clear rooms, choose a reward, push deeper.
- **Abilities system** – unlock/upgrade skills that modify attacks, movement, and utility.
- **Character stats** – increase Health, Damage, Attack Speed, Movement Speed, Crit, and more.
- **Enemy AI** – melee/ranged archetypes with state-based behavior.
- **Boss encounter** – unique arena and multi-phase patterns.
- **Room progression** – sequence of combat rooms with reward choices and a boss gate.
- **Responsive feel** – tight movement, dash, hit reactions, and readable timing.

---

## 🧩 Gameplay Loop

1. **Enter a room** → combat starts.  
2. **Defeat all enemies** → “Room Cleared.”  
3. **Choose a reward**:  
   - **Ability** (new or upgrade), or  
   - **Stat boost** (e.g., +Damage, +Health, +Haste).  
4. **Advance to the next room** → repeat and build your run.  
5. **Boss room** → survive patterns and phases to win the run.

---

## 🛠 Tech Stack

- **Unity**: 2022.3 LTS or Unity 6 (tested locally)
- **Language**: C#
- **AI/Navigation**: NavMesh/state machine–driven behavior
- **Data**: ScriptableObjects for stats/abilities (where applicable)
- **Version Control**: Git + GitHub

---

## 📁 Project Structure

```
Assets/
  Art/                     # Sprites, VFX, UI visuals
  Prefabs/                 # Player, enemies, projectiles, UI, room prefabs
  Scenes/                  # Gameplay scenes and boss arena
  Scripts/
    Abilities/             # Base ability class + individual abilities
    Combat/                # Damage handling, crit logic, hit effects
    Enemies/               # Enemy AI states, movement, attack logic
    Player/                # Movement, dash, input, player stats handler
    Rooms/                 # Room controller, wave logic, progression
    Systems/               # GameManager, run progression, global events
    UI/                    # HUD, reward choice UI, popup feedback
  ScriptableObjects/       # Stat & ability definitions (where applicable)
ProjectSettings/
```



