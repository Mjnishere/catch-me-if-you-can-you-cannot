# Catch the Target

### Your mouse has 30 seconds to prove it has a purpose.

**Catch the Target** is a reaction-based browser game where targets appear, disappear, explode, punish you, reward you, and generally question your hand-eye coordination.

The objective is painfully simple:

> **Click the target.**

Unfortunately, the target has other plans.

---

## What Is This?

A small arcade-style game built entirely with **HTML, CSS, and JavaScript**.

You get a limited amount of time, a limited number of lives, and an unlimited supply of opportunities to click the wrong thing.

There are multiple target types, progressive difficulty, combos, power-ups, particle effects, sound effects, persistent high scores, and enough screen shake to make a missed click feel personally insulting.

---

## How To Play

1. Pick a difficulty.
2. Click **Start Game**.
3. Find the target.
4. Click it.
5. Repeat until either:

   * the timer reaches zero,
   * you run out of lives,
   * or your mouse starts questioning your life choices.

That's it.

No tutorial tree.
No skill points.
No 47-page lore document.

Just click the circle.

---

## Difficulty

Choose your preferred level of suffering.

| Difficulty | Target Size | Time | Lives | Target Speed |
| ---------- | ----------: | ---: | ----: | -----------: |
| Easy       |        60px |  45s |     5 |         Slow |
| Medium     |        45px |  30s |     3 |       Normal |
| Hard       |        30px |  20s |     2 |         Fast |

The game starts on **Medium**, because apparently optimism is the default setting.

The difficulty configuration is built directly into the game logic.

---

## Know Your Targets

### Regular Target

**+1 point**

The normal one.

You see it.
You click it.
Everyone goes home happy.

### Bonus Target

**+3 points**

The shiny one.

Naturally, your brain will immediately decide that missing this would be unacceptable.

### Bomb

**-2 points + lose a life**

It looks suspicious for a reason.

Clicking it removes two points, costs a life, breaks your combo, and gives the screen a small existential crisis.

### Power-Up

The game's way of saying:

> "Fine. You can have something nice."

Power-ups can:

* Freeze the timer for 5 seconds
* Double your points for 8 seconds
* Make targets 50% larger for 6 seconds

Because sometimes the game feels generous.

Sometimes.

---

## Combos

Hit targets consecutively and build a combo.

Every **5 consecutive hits** gives you an additional combo bonus equal to your current combo count.

So if you're sitting at a 10x combo, the game throws another 10 points at you.

Miss a target?

**Combo gone.**

Click the wrong thing?

**Combo gone.**

Click a bomb?

**Combo, points, and one entire life gone.**

The game has standards.

---

## Level System

Every **10 successful target hits**, you level up.

And because success must always have consequences, targets become smaller and spawn faster as you progress.

The game keeps increasing the pressure until the targets are basically asking:

> "Do you actually need to see me?"

The target size and movement interval are progressively adjusted as levels increase.

---

## Scoring

The scoring system is deliberately simple:

```text
Regular Target     +1
Bonus Target       +3
Bomb               -2
Combo Bonus        +combo count
Double Points      2× normal points
```

The goal isn't to understand the economy.

The goal is to make the number go up.

---

## Your Performance Gets Judged

When the game ends, you don't just get a sad little:

**GAME OVER**

You get statistics.

The game records:

* Final Score
* Targets Hit
* Accuracy
* Best Combo
* Level Reached
* High Score

So even if you completely collapse under pressure, you get a detailed report explaining exactly how badly it went.

---

## High Scores

High scores are saved using **browser localStorage**.

That means your score survives between sessions on the same browser.

The game also keeps separate high scores for each difficulty.

So technically, you can become a legend.

A very small, browser-local legend.

---

## Visual Effects

Because clicking circles wasn't dramatic enough.

The game includes:

* Animated gradient background
* Particle explosions
* Floating score indicators
* Screen shake
* Miss flash
* Combo animations
* Level-up animation
* Power-up banners
* Target animations
* Responsive UI

Every successful click gets a little celebration.

Every bomb gets a little punishment.

Every miss gets absolutely nothing except regret.

The visual effects and animations are implemented directly in the CSS and JavaScript.

---

## Sound

The game uses the **Web Audio API** to generate sound effects directly in the browser.

Different events have different sounds:

```text
Hit
Bonus
Bomb
Power-Up
Miss
Level Up
Game Over
```

No external audio files required.

Your browser synthesizes your victories and failures in real time.

---

## Pause

Need to pretend you're doing something productive?

Press:

```text
SPACE
```

Or use the Pause button.

The game stops, the overlay appears, and you can resume when you're ready to return to the extremely important business of clicking circles.

---

## Tech Stack

This project deliberately keeps things simple.

**Frontend**

* HTML5
* CSS3
* Vanilla JavaScript

**Browser APIs**

* Web Audio API
* LocalStorage
* DOM APIs
* CSS Animations
* Web Animations API

No framework.

No build system.

No 400 MB `node_modules` folder sitting in the corner judging you.

Just open the HTML file and play.

---

## Running Locally

Clone the repository:

```bash
git clone <your-repository-url>
cd <repository-name>
```

Then open:

```text
game2.html
```

in your browser.

That's genuinely it.

No:

```bash
npm install
```

No:

```bash
pip install -r requirements.txt
```

No:

```bash
docker compose up
```

No ritual sacrifice to the dependency gods.

---

## Project Structure

At its simplest:

```text
.
└── game2.html
```

The entire game currently lives inside a single HTML file, including:

* UI
* Styling
* Game logic
* Difficulty configuration
* Scoring
* Power-ups
* Audio
* Animations
* High-score storage

One file.

One target.

Several ways to embarrass yourself.

---

## Why This Exists

Because sometimes you don't need another CRUD application.

Sometimes you just need to click a circle very quickly and discover that your reaction time is considerably worse than you thought.

---

## Future Ideas

Potential upgrades:

* Global leaderboard
* Multiplayer mode
* More target types
* Custom difficulty
* Mobile touch optimization
* Achievement system
* Daily challenges
* Different game modes
* More ridiculous power-ups
* Target skins
* Online score sharing

And possibly a mode where the targets stop moving.

But that would probably be too easy.

---

## Final Objective

There is no grand story.

No chosen hero.

No ancient prophecy.

No villain.

Just you.

And a target.

**Click faster. Miss less. Don't click the bomb.**

Good luck.
