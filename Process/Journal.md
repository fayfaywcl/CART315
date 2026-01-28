# Journal

## Week1 Make-A-Thing
 
At the beginning of the idea phase, I was inspired by a tiny game example called “Tesla AI Training Mode”, which itself was based on the MIT Moral Machine Test. This made me want to create a small game rooted in a classic puzzle or childhood logic game. At first, I considered several ideas, such as item collection, passing a ball, or even something like “Crossy Road”. However, after deciding to work in Bitsy, I realized some of these ideas were not practical. Bitsy makes scrolling backgrounds tricky, and a ball-passing game would probably end after just one round.

Because of these limitations, I decided to focus on a logic-based, level-up style game. This worked better with Bitsy’s structure and allowed me to build increasing complexity across levels. To keep everything organized, I created a Notion document to track clues, storylines, and level setups.

Core Game Idea:
- The player is trapped in a mysterious structure.
- Each room contains multiple doors (not always the same number).
- Some characters lie. Some tell the truth.
- Only one door in each level allows progression.
- The player must learn rules, not guess randomly.

Level Setup (Original):
-	Level 1: Two-door riddle (2 identical doors, horizontal line) – 2 guards
-	Level 2: Three-door riddle (3 identical doors, horizontal line) – 2 guards
-	Level 3: Five-door riddle (5 identical doors, horizontal line) – 4 guards
-	Level 4: Escape room (find key in box) – hint box
-	Level 5: Four-door riddle (color-based)
-	Level 6: Five-door riddle (shape-based)
-	Level 7: Maze to find the door

#### What Worked Well
Surprisingly, the core logic of the game actually works. Players can move through levels by choosing the correct door, and choosing the wrong one reliably ends the game. This sounds simple, but getting the flow to work without breaking anything felt like a win. The walls, door placement, and one-way paths help guide the player naturally, so they do not wander off or break the intended experience.

The rule explanations and guard dialogue also work well enough to support the “Two Doors Riddle” logic. Players are given information, and whether they trust it or not becomes part of the challenge.

The overall atmosphere turned out better than expected. The color choices and background music create a mysterious mood without being distracted. I originally planned to include jump scares but later realized they did not fit the game. Shifting toward a “final castle” feeling (like the final fight in a Mario game, Bowser’s castle) made the experience more playable and less frustrating.

#### What Didn’t Work
One level was supposed to be based on choosing the correct door by color. In theory, it was a good idea. In practice because Bitsy’s color system applies to the entire room, I could not assign different colors to individual door sprites. After searching tutorials, watching videos, and asking AI, I still could not find a solution. At that point, removing the level felt healthier than continuing to fight the tool. The game went from seven levels to six, and the overall tone of the game was not affected much, so I think this was the best choice.

#### Challenges Encountered
1.	Color Choices and Contrast
As I wanted a mysterious vibe, so I started with purple for the building blocks. Unfortunately, purple does not always cooperate with other colors. The blocks blended into the background more than I expected, which made the space harder to read. I ended up testing different background colors using Adobe Color until the contrast actually worked. 
 
 

2.	Door and Exit Logic Confusion
Because this was my first time using Bitsy, I built all the rooms before fully understanding how exits worked. I did not know doors could have logic attached to them, so I created one-way paths and placed invisible exits before the doors instead. Later, I realized the “correct” way to do it. While my solution was a bit messy, it had one unexpected benefit, which is players do not instantly “die” by barely touching a wrong door.
 

3.	Ignoring Rules	
During the game testing, I realized that some players completely ignored the rules and guessed randomly. This was not how I wanted the game to be played, since the core idea is logic-based problem solving. To address this, I added hint NPCs (the cloud-shaped characters) at each level to explain the rules or give small tips. However, testing again showed that players could still skip all the hints and continue guessing anyway. To fix this at least partially, I added a rule in the main starting room that forces the player to view the first hint before opening the door and entering the game. I considered doing this for every level, but the logic became much more complicated. I would need to track whether the player read the hints, whether they also read all the guards’ dialogue, and then unlock the doors based on that. Since each level has slightly different logic, this quickly stopped being a universal rule system. In the end, I decided to let the doors work normally (except for the room escape section and the main starting room). The idea became “I already warned you, if you ignore the hints, you are choosing to guess, and guessing has a high chance of failure”. I am not sure this is the perfect solution, but it supports the original idea of the game and worked reasonably well during testing.
 
4.	Naming Organization
Since all guards in the game look the same, and all hint NPCs use the same cloud appearance, while they each have different dialogue. This made organization more difficult than expected. At first, I used long and descriptive names for each character, but this quickly became time-consuming and hard to check, especially when looking at the scene as a whole.To solve this, I switched to a simple naming pattern such as “T1_guard1” or “F1_guard2,” meaning Level 1 guard1 who tells the truth, or Level 1 guard2 who lies. This system made it much easier for me to check whether a guard was saying the correct dialogue and appearing at the correct level.

5.	Using AI as assistance for Dialogue and Logic
For the hints and guards’ speech, I first wrote everything myself. Later on, because I wanted the game to feel more mysterious and require more logical thinking from the player, I asked AI for some help. For storytelling and general tone, it actually did a pretty good job. However, for the rules and guard dialogue, I only used some of its ideas and still had to fix and adjust the logic myself.I would say AI helped speed up the game-making process, but since I already had my own ideas in mind, I still needed to fine-tune its suggestions to make sure everything worked the way I wanted.



Overall, while there are still many parts that could be improved, the final game reflects my original idea, which I feel pretty satisfied with!!!


## Week2 (23-1-2026 to 28-1-2026)
 	


           



