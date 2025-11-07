# Divine Sin

**Divine Sin** is a **Hades-style action roguelike** built in **Unity**.  
The game focuses on **fast, responsive combat**, **stat-driven build variety**, and **room-based progression**, where every run feels unique and player decisions shape the playstyle.

You fight through linked combat arenas, defeat enemies, collect upgrades, and push deeper toward a boss encounter — growing stronger through a scalable stat and ability system.

---

## 🎮 Core Gameplay Pillars

| Pillar | Description |
|-------|-------------|
| **Fast, Responsive Combat** | Dash, sprint, attack, and cast abilities with immediate, fluid control. |
| **Ability & Stat Scaling** | Build variety through new abilities or stat upgrades after each room. |
| **Room-Based Progression** | Fight, clear, choose your reward, move forward — repeat the roguelike loop. |
| **Skill-Based Survival** | Success depends on movement, timing, and decision-making. |

---

## 🔥 Core Features (Detailed)

### ⚔️ Player Combat & Abilities
- Camera-relative movement with smooth acceleration & responsive dash.
- Skill system supporting:
  - Damage abilities
  - Debuffs / DoT effects
  - Heals and lifesteal
  - Ranged skill throws
  - Area-based spell effects
- Animation-event-driven timing for precise combat feel.

### 🌌 Power-Up Reward System (Hades-Inspired)
After clearing a room, you choose one of several upgrades:
- **Stat Boost** (e.g., +Haste, +Crit, +Vitality, +Move Speed)
- **Ability Upgrade** (enhance or modify existing abilities)
- **New Ability Unlock**

Each run allows new **synergy paths** and **playstyle identities**.

Flow:
## 🧠 Modular Stat System

All core stats are defined as **ScriptableObjects**, making balance and tuning easy.

**Stats Include:**  
`Haste · Critical · Mastery · Vitality · Armor · Mana · Movement Speed`

**Flow:**
```text
StatOS (Scriptable Data)
        ↓
BaseStats (Starting Player Values)
        ↓
RuntimeStats (Dynamic, Modified During Run)
        ↓
Abilities & UI Update Automatically


Benefits: **extendable**, **maintainable**, and **easy to balance** without touching core code.

### 🤖 Enemy AI with Finite State Machines
Each enemy is composed of focused states (e.g., **Chase**, **Attack**, **Hit**, **Death**) managed by a shared **EnemyStateMachine**.  
Current archetypes:
- **Mutant** — pressure melee unit (chase/attack loop, hit reactions)
- **Archer** — ranged kiter with **reposition** behavior and projectile **Arrow**
- **Warlock Boss** — multi-phase fight with distinct **move/attack** patterns and arena pacing

FSMs keep behavior modular, debuggable, and easy to extend.

### 🧱 Room & Level Progression
- Rooms define enemy spawns, waves, exits, and next-room routing.
- **RoomManager** tracks enemy defeat; **PortalSpawner/EnemySpawner** handle transitions.
- Supports linear flows today; designed for branching paths and randomized runs.

---

## 🧩 System Architecture Overview

### Ability System

