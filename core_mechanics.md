# Combat System Design  Core Mechanics

Rings of the Damned features a high-speed, aggressive combat system blending the movement fluidity of *Ultrakill* with the gritty brutality of *DOOM*. This document outlines the foundational systems that drive player and enemy combat.

---

# Rings of the Damned – Combat System Core Mechanics

## 1. Player Movement

| Mechanic         | Description |
|-----------------|-------------|
| Base Speed       | 1.2× standard FPS pace (fast, responsive) |
| Jump Height      | Moderate; floaty for air control |
| Double Jump      | Unlocked after defeating Valentina (Lust Circle) |
| Dash             | 1.0s cooldown, 8 directions, usable mid-air |
| Wall Jump        | Unlockable or ring-enhanced (e.g., Heresy Ring) |
| Slide            | Long-distance low-profile slide; chains into dash |
| Mid-Air Control  | Slight steering allowed mid-jump |
| Movement Kill Bonus | Kill during slide or dash restores minor HP or energy |

**Design Notes:**  
- Momentum chaining (Dash → Slide → Wall Jump → Attack) grants small bonuses.  
- Ring-enhanced movement provides visual cues (trails, particle effects).  

---

## 2. Weapon System

| Slot    | Function |
|--------|---------|
| Melee   | Close-range, fast kills |
| Ranged  | Guns, crossbows, energy weapons |
| Magic   | Ring-triggered abilities or channel spells |

**Firing & Attacks:**  
- Light and heavy attacks per weapon.  
- Alternate fire if supported.  
- Ammo replaced by **Blood Gauge (melee)** and **Soul Energy (magic)**.  

---

## 3. Parry System

| Feature | Details |
|---------|---------|
| Timing  | 2-frame window for high-skill parries |
| Effect  | Staggers enemies; emits directional shockwave |
| Projectile Parry | Reflects incoming projectiles |

**Ring Synergy:**  
- Rings can modify parry (e.g., Lust Ring adds charm AoE).  

---

## 4. Ring Mechanics

| Feature       | Description |
|---------------|-------------|
| Equip Limit   | 2 rings at a time |
| Ring Swap     | Swap one ring mid-combat (3s animation) |
| Ring Bonuses  | Active while equipped |
| Debuffs       | Linger until manually removed |

**Strategic Notes:**  
- Ring choice affects enemy behavior, combat loops, and environmental interactions.  

---

## 5. Execution System

| Trigger           | Enemy HP <10% (bosses <5%) |
|------------------|---------------------------|
| Effect            | Execute with melee to restore HP or Blood Gauge |
| Combo Bonus       | 5+ executions within 15s → 1.5s invulnerability |
| Ring Modifiers    | Alter animation, effects, or bonuses |

---

## 6. Enemy AI Design

| Enemy Type        | Traits |
|------------------|--------|
| Low-Tier Mobs     | Fast, easily staggered, keep player moving |
| Elite Enemies     | Complex behaviors, tanky, heavy-hitting |
| Bosses            | Learn player patterns, delayed parry bait, forced movement |
| Adaptive AI (Layer 4+) | React to equipped rings, mimic last ability used (bosses/mini-bosses only) |

---

## 7. Combat Loops

| Loop Type | Example Sequence | Notes |
|----------|-----------------|-------|
| Mobility Combo | Dash → Slide → Melee Chain → Execution | Rewards momentum chaining and skillful positioning |
| Ring Combo | Ring Swap → Magic AoE → Parry → Ranged Follow-Up | Encourages tactical ring management and synergy |
| Execution Chain | Multiple executions in a short time | Grants temporary invulnerability and resource refill |

---

## 8. Future Synergy System (Planned)

| Synergy Type       | Example |
|------------------|--------|
| Ring + Weapon      | Lust Ring + Twin Daggers → Bleed stacking |
| Ring + Arena       | Treachery Ring in Layer 9 → hidden traps/dialogue triggers |
| Weapon + Parry     | Charge weapons double effect after perfect parry |

---

## Notes for Devs

- Core mechanics targeted for **pre-alpha prototype**.  
- Prototype combat loops: mobility → melee → execution → ring → ranged/magic.  
- Visual & audio feedback critical for speed perception and fluidity.  
- Balance testing required for: ring fusion + adaptive AI + execution chains.  

*This document will evolve as testing and engine implementation progresses.*
