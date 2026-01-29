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


## **Week2** (23.1.2026 to 29.1.2026) – Unity 3D Movements 

This week, I started by reading and watching the class materials to understand the focus for the week. From that and this week design journal guidelines , it seems that we would be working mainly with movement, colliders, and basic interaction, so I planned my exploration around those topics. Since I’m more interested in 3D, I decided to focus entirely on Unity’s 3D workflow. 

My idea for this week was to build a small prototype to test basic movement, interaction, and physics working together in Unity 3D.

I began by exploring YouTube tutorials related to 3D and movement. I tried a [first-person movement tutorial](https://www.youtube.com/watch?v=f473C43s8nE) first because it looked engaging and looked like I could learn the code quickly. However, while following it, I realized I had forgotten many Unity basics, such as where to find certain settings and how the editor is organized. (Also ,I only tried 2D mode before , maybe it’s also the reason why it was hard for me to catch up with the 3D workflow at first.) So, at that point, I noticed that copying a video without fully understanding the Unity editor was slowing me down.

To fix this, I switched to Unity’s official [Unity Learn tutorials](https://learn.unity.com/) which I found on internet randomly, it called  [Unity Essentials pathway](https://learn.unity.com/pathway/unity-essentials?version=6.3), which includes guided practice directly inside Unity, especially a section call [movement script](https://learn.unity.com/pathway/unity-essentials/unit/programming-essentials/tutorial/add-a-movement-script?version=6.3)( which I am looking for ).  This really helped me rebuild my foundation, especially around movement, colliders, and Rigidbody.

There is one issues that I initially struggled to find the Unity Essentials project, but after returning to the Editor Essentials tutorials ( the first tutorial in the series) , I realized it must be opened through [Unity Hub](https://learn.unity.com/pathway/unity-essentials/unit/editor-essentials/tutorial/open-the-unity-essentials-project?version=6.0). Once that was resolved, the tutorials aligned correctly with my workspace.

- Note to self: any unknown/unfamiliar material showed in the tutorial, find the creator or the beginning tutorial of that series first.That’s may helps !

As I worked through the tutorials, I learned a lot of the editor itself , including flythrough mode, camera alignment, and working with child objects and pivots. These tools made scene navigation and setup much more efficient for me!

As part of understanding physics, I built a bouncy ball that hits and knocks down tower blocks. This helped me clearly see how Rigidbody, colliders, mass, and physics materials affect gameplay. I also explored different lighting, background settings, and camera angles throughout the process.

  ![BounceBall](Media/BounceBallHitblocks.gif)

I also followed a tutorial to add a frame object and put a cat image inside it. While following the tutorial, it felt like completely new knowledge, even though I had done similar things before. This made me realize how much I had forgotten simply because I hadn’t used Unity in a long time, especially the 3D version. It shows that why going through structured tutorials again was necessary instead of relying on memory.

Also, since the tutorial also include an audio section , I experimented with audio by adding audio sources to game objects, setting background sounds, placing random bird sounds outside the main area, and testing Audio Reverb Zones to improve atmosphere. ( It is a useful skill that I think I could implement in my future prototype)

From there, I implemented several gameplay systems: movement scripts using child objects, rotating collectible items, a collect function with visual effects, jumping, and doors that open when the player(the vacuum cleaner) approaches using triggers and tags.

 ![Collect&jump&dooropen](Media/JumpAndOpenDoor.gif)

After finishing the tutorials and individual experiments, I wanted to check whether I actually understood what I learned. Instead of following another guide, I built a small original prototype using only the systems I had practiced during the week.

- first-person movement
- a child camera
- jumping
- collectible objects (with rotation and effects)
- a simple environment built from square shapes

  ![Gameplay Demo](Media/Week2OwnGame.gif)

The visuals are very basic, but all systems work together, which confirmed that I understood how the components connect. So is Greattttt!!!!! And I also did a small prototyoe as met my expectations for this week

During this process, I noted several common issues and technical reminders that will be useful for future prototypes:

- Remember to set colliders to "Is Trigger" if want the player object to pass through an object while still detecting interactions

- Assign the correct "Tag" to an object if code uses tags for comparison [Common Error that I faced]

- "Box Colliders" should be set slightly larger than the object. If the collider is too small, the player may collide with the door before it has time to open

- If a bouncing ball gets stuck inside another object, it is likely because the object does not have a "Mesh Collider"
  - Reminder: make sure the Mesh Collider component is added and enabled

![MeshCollider](Media/MeshCollider.png)

- ShortCut: **Ctrl + Shift + F**: Aligns the camera to the current view angle

![CameraAlign](Media/CameraAlign.png)

### Next Steps

Now that I’ve caught up on many of the basics, I plan to go back to the first-person movement video and other external tutorials. With a stronger foundation, I think I’ll be able to understand them more deeply and customize them instead of just following along.

Also, there is a issue I faced in the small prototype that is player (the UFO object) flipping when landing on uneven surfaces. Since the Rigidbody can rotate during jumps , it may causes the player to fall over and get stuck. There maybe a chance that the problem come from other sessions too , so I will keep figuring it next week 

  ![GameObjectFlip](Media/GameObjectFlip.png)

Overall, this week felt like a strong process approach: reading class materials first, choosing focused goals, using structured tutorials, and then experimenting on my own. If I had only relied on self-discovery and random tutorials, I would have spent most of my time debugging unknown issues without understanding why things weren’t working. I wouldn’t have been able to learn as efficiently as I did this week. 

This made it much easier to focus on learning the actual systems instead of fighting the tool.

So , Keep Moving On !!! and Learn Smartly 😉
 	
