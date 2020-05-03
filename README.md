# Random map generation

## Introduction

In this webpage you will find all the information about the random generation of maps in video games.

## Procedural generation

In computing, procedural generation is a method of creating data algorithmically as opposed to manually, typically through a combination of human-generated assets and algorithms coupled with computer-generated randomness and processing power. In video games, it is used to automatically create large amounts of content in a game. Depending on the implementation, advantages of procedural generation can include smaller file sizes, larger amounts of content, and randomness for less predictable gameplay. Procedural generation is a branch of media synthesis.

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




You can use the [editor on GitHub](https://github.com/LordUnicorn31/Random_map_generation/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/LordUnicorn31/Random_map_generation/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
