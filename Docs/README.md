# Random map generation

## Introduction

Welcome everybody,I'm Jordi Espriu and I'm a student of the CITM in Barcelona. In this webpage you will find all the information about the random generation of maps in video games.

## Procedural generation

In computing, procedural generation is a method of creating data algorithmically as opposed to manually, typically through a combination of human-generated assets and algorithms coupled with computer-generated randomness and processing power. In video games, it is used to automatically create large amounts of content in a game. Depending on the implementation, advantages of procedural generation can include smaller file sizes, larger amounts of content, and randomness for less predictable gameplay. Procedural generation is a branch of media synthesis.

![Image](https://gamepedia.cursecdn.com/minecraft_gamepedia/thumb/d/d4/Jungle_River.png/1200px-Jungle_River.png)

### Applications of procedural generation

-Terrain/level creation

-Enemies/spawning

-Loot/weapons/gear

-Models/textures/animations

-Sound/music

-Story/quests/dialog

### Full randomness

While not intelligent, you can use pure randomness.

-How big is each level of our dungeon? Randomly create a grid of tiles 10-100 high/wide.

-What is the layout of the dungeon? Each tile is randomly selected from a list: Empty, Decoration, Trap, Enemy.

-What enemies are going to show up? Randomly select 1-10 enemies.

-What loot drops? Pick a random item image, select 5 random abilities for it.

### Guided randomness

As we just saw, complete randomness can be great… or disastrous. Instead of drowning our game in randomness we’ll selectively apply randomness, with limits (or ranges). Good games slowly ramp up difficulty and avoid huge discrepancies in difficulty. Let’s take our last example and upgrade it:

-How big is each level of our Dungeon? The level grid starts at 10x10 and gets increasingly bigger as the player progresses.

-What is the layout of the dungeon? Each level is allowed a certain number of traps and decorations. Those numbers slowly increase with  the level size so the whole level doesn’t become traps and decorations.

-What enemies are going to show up? Start with only weak enemies and slowly introduce the more difficult ones. Optionally replace a harder enemy with many smaller ones, for more variety.

-What loot drops? Find a way to categorize the abilities that can appear on an item and select 1 from each category. Maybe certain abilities have a higher chance to appear together and maybe some can’t appear together at all. Fire and Ice damage on a single weapon might seem silly for example, cuz realism.

-Quests - “Fetch ______ ______’s from ______ for ______”.

### Seeds

The seed is a value that it used at the starting point when generating a random map. This seed is a value.

Yes, sounds cool, but why should we care about this number? Well, the answer is easy, we care about this number because it represents a specific configuration of the map we are creating. What it means is that whenever we put the same seed the same map will always be created. Eventhough it is not a must in a video game it is always cool to have this option so that the player can investigate and look for cool seeds to share with other people. Keep in mind that eventhough the map is the same each player can play in a different way and use the map and resources in a different way.

### Pre-generated features

Let's put a dungeon crawler game as an example to see this topic.

·Dungeon Layout - Create “blocks” that consist of several tiles preconfigured with decorations, traps, and enemies. Imagine 4 Skeleton Guards faithfully guarding a booby-trapped sacred altar with a Golden Chalice on top. Sounds cool, right? (The Division, Diablo, and Spelunky all do something like this.

·Loot - Create Named Weapons that have unique stats like “The Party Pooper” which is the only weapon in the game that makes a sad trombone noise and spews out confetti every time you kill an enemy. (The Division, Diablo, Borderlands, and many others have named items)

·Quests - Hand-craft a number of quests and sprinkle them throughout the game amidst the fetch quests. A cool idea might be to disguise a set-quest as a fetch quest, surprising the player with a boss or some awesome loot.

![Image](https://media.moddb.com/images/articles/1/230/229234/auto/34507-utero_xl_bindi.jpg)
## Cool, but how can I apply this to my own games? (Design)

Well, first of all you need a design stage to decide what will be random and what will not, this is basically because randomness is a really cool feature but could be deadly when used wrong.

For example, let's say we want to create a dungeon-like game. In this game there are ores that can be found in the mines, enemies, and drops/loots (apart from other things that we won't consider in this example).
So, with this example we will learn to "force" randomness in order to have a balanced game.
First of all, we will consider that the number of rooms is not limited by any number (kind of minecraft style). What this means is that we aren't forcing the game to have any output, we tell it to create a random map with a random number of rooms and it does so. But can we do this with all the features of the game? I don't think so and I will explain you why.
Now we are puting the ores in the map, in this case it is not a good idea to let the game decide which number of ores it should put in the map. In this case we should force the game to put certain number of each ores and we will work with percentages in order to put the ores (Imagine playing minecraft and half of the map being diamonds!). The percentages are usefull because it allows us to balance the game e.g: 1% daimonds, 5% gold, 15% iron, 79% dirt. Now that looks more like a balanced game!

With this done we should have an idea of how to design a game that is going to be random.

## Cool, but how can I apply this to my own games? (Programming)

Now that we have our design done we will proceed to programm the game. In this example we will use the "random" library from visual studio.


### Links and references

[Basic video about Procedural Generation](https://www.youtube.com/watch?v=-POwgollFeY&t=175s​)

[Building worlds in No man's sky](https://www.youtube.com/watch?v=C9RyEiEzMiU)


