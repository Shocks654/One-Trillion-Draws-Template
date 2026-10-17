# Chapter 7: Modifying game logic
You will now change:
* draws
* rarity

## How to change draws?
It is in the front of js/logic.js
## How to change rarity?
In both js/consts/effect.js, and js/logic.js
    cardRChance: 1e-3,
    cardSRChance: 0.99999e-5,
    cardSSRChance: 0.99999e-7,
    cardURChance: 0.99999e-9,
So the game is treating these as weights:

Normal = 1
Rare = 0.001
Super Rare = 0.0000099999
Super Super Rare = 0.000000099999
Ultra Rare = 0.00000000099999
That means:
Normal has a very big chance to appear, so the smaller the weight (between 0 and 1), the rarer it is!
let rarityList = ["ur", "ssr", "sr", "r", "n"];
    let rarityChance = { n: 1, r: effects.cardRChance, sr: effects.cardSRChance, ssr: effects.cardSSRChance, ur: effects.cardURChance }
    let chanceSum = 0;
rarityList has all the raritys.
[Chapter 8](Chapter-8-Saving-and-sharing.md)