# Forest Dou Dizhu 森林斗地主

A cute cartoon card game based on **Dou Dizhu**, a classic Chinese card game where one landlord plays against two farmers. Pick a character from the **Forest Snack Squad** and play against two AI friends. The goal is to win pinecones.

**Play online:** https://sf-ryanyan.github.io/Forestdoudizhu/

---

## Overview

Forest Dou Dizhu is a single-player web game. You play against two AI opponents, and each one has its own personality and play style. A match lasts until one player runs out of pinecones. Then a final ceremony names the big winner.

The game runs entirely in the browser. You do not need to install anything, and there is no server and no login. The interface is in Chinese.

---

## Features

- **6 original characters**: each one has its own play style and facial expressions (smug, nervous, happy, crying)
- **3 difficulty levels ("spice levels")**: Mild Sweet, Medium Spicy, Extra Spicy. At Extra Spicy, the AI tracks played cards, works with its teammate, and tries to block your last card.
- **3 match lengths ("portion sizes")**: Small, Medium, Large
- **Doubling round**: after the landlord is chosen, each player can double the stakes
- **Turn timer**: there is no hint button, so you plan every move yourself
- **Special effects and sounds** for straights, consecutive pairs, airplanes, bombs, rockets, and Spring wins
- **Final awards**: a winner's podium plus fun titles such as Bomb Maniac and Best Teammate
- **Fair play rules**: no redeals, and leaving in the middle of a round counts as a forfeit

---

## Characters: The Forest Snack Squad

| Animal | Name | Play Style |
|---|---|---|
| Fox | 辣条 Latiao (Spicy Strip) | Bold and risky, loves throwing bombs |
| Panda | 汤圆 Tangyuan (Rice Ball) | Slow and steady, never wastes big cards |
| Orange Cat | 年糕 Niangao (Rice Cake) | Lazy most of the time, explodes at the key moment |
| Shiba Inu | 豆包 Doubao (Bean Bun) | Friendly, the best team player |
| Hamster | 瓜子 Guazi (Sunflower Seed) | Hoards big cards until the very end |
| Bunny | 棉花糖 Mianhuatang (Marshmallow) | Fast hands, loves straights and pairs |

You pick 1 character. The other 2 are chosen at random from the rest.

---

## Contents

```
.
├── index.html   # The whole game: HTML, CSS, and JavaScript in one file
└── README.md    # This file
```

---

## How to Play

1. Open the game in a desktop browser (Chrome, Edge, or Safari).
2. Choose your **character**, **spice level**, and **portion size**, then press Start.
3. **Bid** for landlord: 1, 2, or 3 points, or pass.
4. **Double** or not after the landlord is chosen.
5. **Play cards**: select your cards, then press Play (or Enter). Press Pass (or Space) to skip.
6. The first team to play all of its cards wins the round.

**Controls**

| Action | How |
|---|---|
| Select a card | Click it, or click and drag across several cards |
| Select all cards of one rank | Double-click a card |
| Clear selection | Right-click in your hand |
| Play | Play button or Enter |
| Pass | Pass button or Space |
| Forfeit | Forfeit button (top right) |
| Menu | Main menu, New game, Rules, Sound on/off |

---

## Rules

**Setup**
- 3 players, 54 cards (including 2 jokers). Each player gets 17 cards, and 3 cards are left as the bottom cards.
- The highest bidder becomes the **landlord** and takes the 3 bottom cards. If nobody bids, the first player to bid becomes landlord at 1 point.
- The other two players are **farmers** and play as a team.

**Playing**
- The landlord plays first. Each next player must play the same card type with the same number of cards and a higher rank, or pass.
- If both other players pass, the last player who played starts a new round of any type.
- Card ranks from high to low: Big Joker > Small Joker > 2 > A > K > Q > J > 10 > ... > 3. Suits do not matter.

**Card types**

| Type | Example |
|---|---|
| Single | 5 |
| Pair | 5 5 |
| Triple | 5 5 5 |
| Triple + 1 | 5 5 5 + 3 |
| Triple + Pair | 5 5 5 + 3 3 |
| Straight (5+ cards, up to A) | 3 4 5 6 7 |
| Consecutive pairs (3+ pairs) | 3 3 4 4 5 5 |
| Airplane (consecutive triples, can add singles or pairs) | 3 3 3 4 4 4 + 5 6 |
| Four + 2 | 5 5 5 5 + 3 7 |
| Bomb (beats any normal type) | 8 8 8 8 |
| Rocket (highest of all) | Small Joker + Big Joker |

**Time limits**

| Spice Level | Per turn |
|---|---|
| Mild Sweet | 30 seconds |
| Medium Spicy | 25 seconds |
| Extra Spicy | 20 seconds |

The landlord gets 10 extra seconds on the first turn. Bidding has 15 seconds and doubling has 10 seconds. When time runs out, the game passes for you, or plays your lowest card if you must lead.

**Scoring**

```
Base score = 20 × bid × 2^(number of bombs)   (× 2 again for a Spring)
Each landlord–farmer result = base score × landlord's double × that farmer's double
```

| Portion Size | Starting Pinecones | About |
|---|---|---|
| Small | 500 | 15–20 minutes |
| Medium | 1,000 | 30–40 minutes |
| Large | 2,000 | 1 hour or more |

The match ends when any player runs out of pinecones. The player with the most pinecones is the big winner.

---

## Built With

- Plain HTML, CSS, and JavaScript in a single file, with no frameworks and no build step
- All characters, cards, and icons are drawn with inline SVG
- Sound effects are generated live with the Web Audio API, so there are no audio files
- Confetti, fireworks, and petals use Canvas particles
- Progress and settings are saved only in your own browser (localStorage)

---

## Acknowledgements

- **Dou Dizhu**, the traditional Chinese card game that inspired this project
- **Google Fonts**: ZCOOL KuaiLe, Noto Sans SC, and Fredoka
- Built with the help of AI coding tools

---

## Disclaimer

This game is for entertainment only. Pinecones are play points with no real-world value, and the game does not involve real money or gambling of any kind. All characters and artwork are original. The game does not collect any personal data.

---

## About Me

Hi, I'm **Ryan Yan**, a data analyst. I enjoy building small, fun web projects with AI tools.
