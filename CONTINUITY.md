# Jason's RPG System — Continuity Document

> **Purpose:** This document captures everything about the system's design, mechanics, decisions, and future direction. Use it as the single source of truth when continuing development.

---

## Project Overview

- **Creator:** Jason (system designer), Benjamin (developer/collaborator)
- **Repo:** https://github.com/benjaminmwaldo/rpg-players-handbook
- **Live Page:** https://benjaminmwaldo.github.io/rpg-players-handbook/Players_Handbook.html
- **Source Document:** `rpg.docx` — Jason's original notes and mechanics
- **Output:** `Players_Handbook.html` — Single-file HTML Player's Handbook with embedded CSS

---

## Core Design Philosophy

These are the non-negotiable principles Jason built the system on. Every future addition must respect them:

1. **Tight Math, No Inflation.** Stats start 9–12, grow slowly (cap ~16–18 at level 20). The 3d6 bell curve means even +1 is significant. Never add scaling bonuses that blow up the math.
2. **Every Level Matters.** No dead levels. Every single level grants a new *ability*, not just a number bump.
3. **Simplicity Over Bloat.** Jason explicitly rejects D&D's mechanical bloat. Rules should be easy to remember, easy to run. If a rule needs a paragraph of exceptions, it's probably wrong.
4. **One Resource System.** Stamina is universal. Fighters, Rogues, and Mages all use the same pool differently. Never introduce a second resource currency.
5. **Reactive Combat.** Reactions declared *after* hit roll, *before* damage. This is the core tactical loop — every incoming attack is a decision. Protect this at all costs.
6. **Feats Add Options, Not Numbers.** Feats give you new things to *do*, not passive stat bonuses. Class defines power; feats define style.
7. **No Stat Confusion.** 5 stats (Might, Reflex, Vigor, Sense, Wit) are distinct and non-overlapping. No INT/WIS/CHA mess.

---

## System Mechanics Reference

### The Five Stats
| Stat | Covers | Used For |
|------|--------|----------|
| **Might** | Raw physical power | Melee damage, grappling, bow damage (capped by draw weight), Athletics, Intimidation |
| **Reflex** | Speed and agility | Dodge, initiative, finesse weapons, Stealth, Acrobatics, Sleight of Hand |
| **Vigor** | Toughness/endurance | HP, flinch saves, death threshold, stamina recovery (Fighter), Endurance |
| **Sense** | Awareness/intuition | Ranged accuracy (bows), initiative, Perception, Insight, Survival, Streetwise |
| **Wit** | Intellect/personality/magic | Spellcasting, Lore, Medicine, Persuasion, Deception, Craft, Appraisal |

### Core Roll: 3d6
- **Normal:** 3d6 (average 10.5, bell curve)
- **Minor Advantage:** 4d6 keep best 3
- **Major Advantage:** 5d6 keep best 3
- **Minor Disadvantage:** 4d6 keep worst 3
- **Major Disadvantage:** 5d6 keep worst 3
- **Critical Success:** 2+ sixes
- **Legendary Success:** 3 sixes
- **Auto-Failure:** 2+ ones
- **Critical Failure:** 3 ones

### Key Numbers
- **Starting Array:** 12, 11, 10, 10, 9
- **Modifier Formula:** Stat − 10
- **Proficiency Bonus:** Flat +2 (never scales)
- **Starting Modifier Range:** −1 to +3
- **Guard (AC):** 8 + Armor Bonus + Reflex Mod (limited by armor type)
- **Initiative:** 3d6 + Reflex Mod + Sense Mod + bonuses
- **Movement:** 30 ft standard, 5-ft grid

### Action Economy
- 2 actions per turn
- Reactions consume *next turn's* actions
- Reactions declared after hit roll, before damage roll

### Classes
| Class | HP/Level | Stamina Base | Role |
|-------|----------|-------------|------|
| Fighter | 10 + Vigor | 4 + Vigor | Controls space through combat modifiers |
| Rogue | 8 + Vigor | 4 + Reflex | Creates openings through exploit modifiers |
| Mage | 6 + Vigor | 6 + Wit | Shapes spells through construction modifiers |

### Disciplines (chosen at Level 1)
- **Fighter:** Two-Handed, Duelist, Shield, Archer
- **Rogue:** Ambusher, Predator, Evasionist
- **Mage:** Ritual Caster, Non-Combat Caster, Complex Caster

### Subclasses (chosen at Level 5, features at 5/9/13/17)
| Subclass | Blend | Fantasy |
|----------|-------|---------|
| Warmaster | Fighter pure | Battlefield commander, ally buffs |
| Assassin | Rogue pure | Burst damage, poison, stealth kills |
| Arcanist | Mage pure | Raw spell power, metamagic |
| Skirmisher | Fighter/Rogue | Mobility, hit-and-run |
| Spellblade | Fighter/Mage | Weapon-channeled magic |
| Trickster | Rogue/Mage | Illusions, debuffs, misdirection |

### Magic System
- **6 Forms:** Destruction, Protection, Restoration, Alteration, Divination, Illusion
- **Spell Construction:** Base Effect + optional Modifiers = total Stamina cost
- ~5 Bases per Form, ~4 Modifiers per Form
- Mage disciplines reduce modifier costs in specific ways
- Some spells can be cast as Reactions

### Flinch
- **¼ max HP in one hit:** Vigor save TN 12 or lose 1 action
- **½ max HP in one hit:** Vigor save TN 15 or lose 2 actions

### Death
- At 0 HP: unconscious, lose 2 HP/turn
- Death at: negative (Vigor score + Vigor modifier) HP
- Stabilize: 2 actions, 3d6 + Proficiency vs TN 12
- Wake up: 3d6 + Vigor vs TN 14 each round

### Rest
- **Short Rest (1 hr):** Heal Vigor score in HP, recover half Stamina (round up)
- **Long Rest (8 hrs):** Full HP, full Stamina, clear conditions

### Flanking
- +1 to hit when you and an ally are on opposite sides of an enemy

### Surprise
- Non-surprised act first (full round), then everyone rolls initiative normally
- Surprised enemies are treated as Exposed (+2 damage taken)

### Conditions (10)
Exposed, Prone, Grappled, Stunned, Blinded, Frightened, Poisoned, Burning, Frozen, Silenced

### Races (6)
Human (+1 any, extra minor feat), Elf (+1 Sense, keen senses), Dwarf (+1 Vigor, poison resist), Halfling (+1 Reflex, lucky), Orc (+1 Might, relentless), Tiefling (+1 Wit, fire resist)

### Backgrounds (8)
Soldier, Scholar, Criminal, Artisan, Noble, Outlander, Acolyte, Merchant — each grants 1 skill proficiency + 1 narrative benefit

### Level Progression (1–20)
- **Stat Increases:** 8 total across 20 levels (mix of free choice and "not your highest")
- **Minor Feats:** Levels 0, 3, 8, 14
- **Major Feats:** Levels 6, 11, 16
- **Subclass Features:** Levels 5, 9, 13, 17
- **Stamina +1:** Levels 3, 6, 9, 12, 14, 16, 19
- **Level 20 Capstone:** Second Discipline, stat cap raised to 18

---

## What Was Preserved vs. Created

### Directly From Jason's Notes (Preserved Exactly)
- 5 stats and their names
- 3d6 core roll + advantage/disadvantage system
- Crit/legendary/auto-fail thresholds
- The 3 classes and their resource philosophy
- All 12 discipline descriptions (Two-Handed, Duelist, Shield, Archer, Ambusher, Predator, Evasionist, Ritual Caster, Non-Combat Caster, Complex Caster)
- 6 subclass names and archetypes
- 2 actions/turn, reaction timing
- Initiative formula
- Flinch mechanic (¼ and ½ HP thresholds, TN 12/15)
- Death/stabilization/consciousness rules (exact TNs and mechanics)
- Bow mechanics (Might for damage capped by draw weight, Sense for accuracy, 2-action draw/fire)
- Existing feat names and descriptions (Actor, Alert, Athlete, Close-Quarter Marksman, armor proficiencies, Dual Wielding, weapon type proficiencies, Dual Wield Master, Shielding Master)
- Surprise round rules
- Design philosophy and stated goals
- Stat array: 12, 11, 10, 10, 9
- Skill tree ideas/notes (preserved as future development seeds)

### Created to Fill Gaps (Faithful to Jason's Philosophy)
- **Modifier formula:** Stat − 10 (proposed in plan, implemented)
- **Race details:** Stats, traits, and flavor abilities for all 6 races
- **Background details:** Proficiencies and narrative benefits for all 8
- **Proficiency system:** Flat +2, categories, non-proficiency penalties
- **Full skill list:** 16 skills mapped to 5 stats
- **Weapon tables:** Full simple/martial melee + ranged with properties
- **Armor table:** Light/medium/heavy with Guard values and penalties
- **Guard formula:** 8 + Armor + Reflex (capped by type)
- **Completed feat descriptions:** Grappler, Shielder, Duelist, all Master feats
- **Stamina pool sizes:** Per class (Fighter 4+Vig, Rogue 4+Ref, Mage 6+Wit)
- **Subclass features:** All 6 subclasses at levels 5/9/13/17
- **Full magic system:** 6 Forms with bases and modifiers
- **Level 1–20 progression table**
- **All 10 condition definitions**
- **Rest mechanics:** Short rest and long rest recovery
- **Skill check TN table:** Easy 8 through Nearly Impossible 18
- **HP per level per class**

---

## Technical Notes

### HTML File Structure
- Single file with embedded CSS (no external dependencies except Google Fonts)
- Fantasy aesthetic: Cinzel/Cinzel Decorative for headings, Crimson Text for body
- Dark parchment background (#f4e8c1), dark ink (#2c1810)
- Color-coded class sections: Fighter (red #8b1a1a), Rogue (green #2d4a2d), Mage (blue #1a3a5c)
- 16 chapters with anchor links from TOC
- Responsive (mobile-friendly) and print-friendly
- ~86KB total file size

### GitHub Setup
- Repo: `benjaminmwaldo/rpg-players-handbook`
- GitHub Pages enabled on `master` branch, root path
- Single commit so far; future work builds on this

---

## Next Project: Steampunk / Weird (Lovecraftian) Horror Reskin

### Direction
Transform the generic fantasy base into a **steampunk + Lovecraftian horror** RPG with **gritty realism**. The mechanical core stays; the flavor, themes, and some systems get reworked.

### Initial Ideas to Explore

**Setting & Tone**
- Victorian/industrial era with steam technology, clockwork, and gas lamps
- Lovecraftian cosmic horror: unknowable entities, sanity erosion, forbidden knowledge
- Gritty realism: wounds matter, resources are scarce, death is close
- Moral ambiguity — no clear good vs. evil, just survival and sanity

**Potential New/Modified Systems**
- **Sanity System:** A new track (not a second resource — could be tied to Vigor or Wit). Encountering eldritch horrors, reading forbidden texts, or using certain powers erodes sanity. Mechanical consequences at thresholds (similar to Flinch but for the mind).
- **Corruption/Taint:** Using eldritch power is tempting but leaves a mark. Could tie into the magic system — more powerful spells risk corruption.
- **Gritty Rest Variant:** Short rest = overnight, Long rest = several days of downtime. Makes combat more consequential.
- **Wound System:** Instead of just HP, lingering wounds from critical hits or flinch failures. Broken bones, bleeding, trauma.
- **Firearms:** Steam-powered guns, clockwork weapons. Could use the bow mechanic framework (accuracy stat vs. damage stat, reload actions).
- **Alchemy/Tinkering:** Replace or supplement some magic Forms with steampunk crafting (clockwork gadgets, chemical compounds, steam devices).

**Class Reskins**
- Fighter → **Soldier / Enforcer** (military, industrial muscle)
- Rogue → **Agent / Investigator** (detective, spy, cat burglar)
- Mage → **Occultist / Arcanist** (forbidden knowledge, eldritch pacts)
- Could add or modify subclasses: **Alienist** (Lovecraftian scholar), **Automaton Engineer** (clockwork summoner), **Witch Hunter** (anti-occult specialist)

**Race Reskins**
- Fantasy races may not fit — consider replacing with human-only backgrounds or subtler "bloodlines" / "afflictions" (someone touched by the Other, someone with clockwork prosthetics, etc.)

**Magic Reskin**
- The 6 Forms could become more thematic:
  - Destruction → **Entropy** (decay, disintegration, eldritch blasts)
  - Protection → **Warding** (seals, barriers against the unknown)
  - Restoration → **Alchemy** (chemical healing, stimulants, antidotes)
  - Alteration → **Transmutation / Engineering** (clockwork augmentation, reshaping matter)
  - Divination → **Forbidden Sight** (seeing beyond the veil — at a cost to sanity)
  - Illusion → **Phantasmagoria** (gas-lamp hallucinations, shadow manipulation)

**Horror Elements**
- Fear/dread as a mechanical concept (beyond the Frightened condition)
- Investigation/mystery mechanics (clue gathering, connecting evidence)
- NPC trust/suspicion tracking
- Darkness and light as meaningful tactical elements

### Key Constraints for Next Phase
- **Don't break the core math.** The 3d6 bell curve, flat +2 proficiency, and tight stat range are what make this system work. Any new systems must fit within that framework.
- **Don't add a second resource.** If sanity is a track, it should work differently from Stamina (more like HP — a threshold you don't want to cross, not something you spend).
- **Keep it simple.** Jason's anti-bloat philosophy applies doubly to horror games, which often drown in subsystems. One sanity track, one wound system, one corruption mechanic — not all three. Pick the most impactful.
- **Preserve reactive combat.** The reaction system is the crown jewel. Horror should enhance the tension of those decisions, not bypass them.

---

## File Inventory
| File | Purpose |
|------|---------|
| `rpg.docx` | Jason's original notes (source of truth for his design intent) |
| `Players_Handbook.html` | Complete Player's Handbook v1 (generic fantasy) |
| `CONTINUITY.md` | This document — project memory and future direction |
