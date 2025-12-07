# Tactical Hell
This document's sections are organized according to features the project offers:

1. **Archive**: Doom 2-compatible WADs that you can immediately download and play.
2. **Suggested mods**: a GZDoom mod-list that you can use with the provided WADs and most other WADs and games.
3. **Generating your own WADs**: an Obsidian configuration file you can use to automatically generate new WADs.
4. **Suggested soundtrack**: a number of high-quality, free and/or copyright-friendly music that fits the intended gameplay.

While each one is designed to be part of a greater whole, they are modular and can be used indepedently of each other to your own liking.

## Rationale
I love Oblige and [Obsidian](https://github.com/dashodanger/Obsidian/) but I have struggled to fine-tune settings that feel right for me. Part of it is that I want more depth in a FPS than vanilla Doom can provide and also that I'd rather play WADs as perma-death roguelites than with the more traditional Doom community approach of mastering levels and WADs death-by-death until you know them like the back of your hand.

After re-watching Ross Scott's [Freeman's Mind](https://www.youtube.com/playlist?list=PL6PNZBb6b9LvDWpI-5CPYUxG1Rnm-vr9V) recently, I was thinking about how different Doom and Half-Life are in their design, despite all the obvious similarities and decided that I could try mimicking a more tactical, deliberate WAD setup with Obsidian, compared to the [classic Doom-style ultra-violence](https://youtu.be/HGqMk7iDBR8) the default settings lean towards.

To sum it up, the goal is to have less monsters to fight but have the monsters that are there become a harder challenge, which in the Doom engine basically means having to rely on less than ideal weapons or ammo than you'd like to defeat monsters of a given tier. This is not easy to get right with Obsidian, as there is a lot of fine-tuning involved in the loot and challenge curves and given the high degree of randomness, leeway for worst- and best-case scenarios need also be taken into account, which requires a fair amount of playtesting on its own.

Ultimately, the slower gameplay should reward awareness and planning more than extensive map knowledge and perfect reacton-time. This forces players to use terrain and indirect opportunities to their advantage (such as making the most out of explosive barrels and power-ups). Conserving ammo and quickly deciding what weapon is best for a given situation should also be primary skills in beating these WADs deathless.

Secondary goals for the project and its WADs are to maintain some degree of realism (or as much as a game about getting fire-blasted by alien hellspawn will let you) and also to (on occasion, especially on the final levels of an episode) to allow for that mass-combat, hectic gameplay that only the id Tech 1 engine can really provide and excel at - while not intended as the focus of gameplay, it often works well as a finale.

If this sounds a lot like a personal choice of Obsidian settings that needn't be a public project at all, you're not wrong but if it helps shortcut other people into less spam-heavy, more tactical, high-quality Doom gameplay they may be interested in, then the small overhead of setting up a read-me and repository should be worth it. Also, I sometimes play WADs live [on Twtich](https://www.twitch.tv/tukkek) and if people ask about my setup I can just refer them here!

## Archives
Episodes found on the `WADs/` folder in this repository have been tested and beaten in Ironman style and are the fastest way to enjoy Tactical Hell. The easiest way to get them is to use GitHub's [Download ZIP feature](https://github.com/tukkek/tactical-hell/archive/refs/heads/main.zip) and then extract the folder using your operating-system's default applicatoin or something like [7-zip](https://www.7-zip.org/).

If you happen to find an `obsolete/` folder inside the WAD folder, that means that those have been tested with a previous selection of mods than the currently recommended list in the next section. If they are kept in the archive, they are most likely still playable on their own but they might not have been tested with the latest selection of mods to guarantee they're ironman-friendly or properly balanced in general. If they turn out to be too easy or too hard compared to the most current episodes availabe, try adjusting their in-game difficulty accordingly;

## Suggested mods
This is a list of [GZDoom](https://zdoom.org/index) mods that complement and enhance the main goals of this project. They are entirely optional and the provided WADs can be played without them.

1. [RRMW](https://bitbucket.org/Player701/rrwm/src/master/): replaces vanilla Doom weapons with 1-to-1 alternatives that require reloading. This really takes the depth of Doom's combat to the next level as knowing when it's safe to reload, the rhythm of firing each weapon and its respective loading time (or when to just draw another gun and keep firing instead) makes the game feel much more modern and also provides a nice touch of realism. I personally find the Manual-only reload setting to be the best way to deliver these gameplay enhancements, which can be found in the `RRMW` menu in-game.
2. [Bolognese](https://www.moddb.com/mods/brutal-doom/downloads/bolognese-gore-mod-v20). A cosmetic-only mod that adds a lot of gore to the game, particularly with the bigger weapons and enemies. Since Tactical Hell is all about fighting bigger monsters with less gadgets, this mod really helps deliver those "big" Doom moments when you finally go all-out into ultraviolence - or even just to accentuate the satisfaction of taking down a tough enemy when all you have to rely upon a weaker arsenal!

Gameplay-affecting mods in this section will directly affect a WAD's difficulty, usually making it harder. If you decide to play without using them, consider playing on a higher difficulty level to offset the balance or find the in-game difficulty setting that works best for you.

### Installing [GZDoom](https://zdoom.org/index) mods
While minimally involved, installing mods is not hard. First you will need to install GZDoom, if you haven't already. [Follow these simple instructions](https://zdoom.org/wiki/Installation_and_execution_of_ZDoom#How_to_install_ZDoom) to install the engine and setup `DOOM2.wad`.

Next, open the `doom-<user>.ini` and find the section called `[doom.id.doom2.Autoload]`. Modify it so it looks like this:

```
[doom.id.doom2.Autoload]
PATH=rrwm.pk3
PATH=sm4BBgorev3.pk3
```

Make sure to follow the links on the previous section, download and extract these `.pk3` files to the GZDoom installation directory.

If you are using more or less mods in your own installation, add or remove lines accordingly. (Note: `sm4BBgorev3.pk3`'s authors recommend always leaving it as last in the load order).

If you are using Linux, the configuration file and mod files should are found on `/home/<user>/.config/zdoom/` instead.

## Suggested soundtrack
Here are some amazing, high-octane, DMCA-friendly music that should go well with Tactical Hell:

* [Sauer Anger](https://marcapullen.bandcamp.com/album/sauer-anger) by [Marc "Fanatic" Pullen](https://www.doomworld.com/fanatic/). 
* OverClocked ReMix's [The Dark Side of Phobos](https://ocremix.org/album/4/doom-the-dark-side-of-phobos).
* OverClocked ReMix's [Delta-Q-Delta](https://ocremix.org/album/11/doom-ii-delta-q-delta).

To enjoy these while playing Tactical Hell, mute the in-game music (via Options, Sound Options then the Music Volume slider) and play the tracks using an external media player (such as [VLC](https://www.videolan.org/) or [Clementine](https://www.clementine-player.org/)).

## Balance and testing
This is mostly a discussion on how I test the Obsidian settings found in the provided configuration file, so potential players can know what to expect out of the WADs.

Since WADs included in this repository are episode-length and finding the right settings takes playing multiple WADs fully, I will often test them on a lower difficulty (Not too rough). If I can beat the WAD on my first try, while playing fairly casually, then it is likely to be added to the archive. I also consider ending most levels with high health and a reasonable amount of surplus ammo to carry over to be a good sign that the WAD would also be Ironman-friendly on the default difficutly (Hurt me plenty).

Aiming towards the "normal" difficulty should mean that there is a lot of leeway to both players of higher and lower skill ceiling than myself, with or without using the mods suggested above. Since I cannot possibly find a balance that will please everyone at the same time, shooting for the middle and letting individual players find their own preferred difficulty setting seems like the next-best approach.

### Semi-permadeath approach
All WADs generated for this project use the "pistol start" Obsidian option, which means every level should be beatable with a fresh start (pistol only). If you die and want to continue playing or simply isn't interested in full permadeath, you can always try restarting a level in this manner, which adds enough challenge to a level after death, compared to coming in fully lock-and-loaded from the previous maps.

Sadly, as far as I know, GZDoom doesn't support this natively but you can either:

1. Type `/map *` in the console after you die; or...
2. Type `/bind p "map *"` to make it so every time you hit `p` in your keyboard, the level will restart with a pistol-only start, Feel free to replace `p` with any letter of key of your choosing, inclduing function keys like `f1`, `f2`...

To see and change which key opens the console, open the in-game menu, then choose Options, Customize Controls, Other and finally Open Console.

## Generating your own WADs with Obsidian
This version of Tactical Hell is compatible with [Obsidian's v20](https://github.com/obsidian-level-maker/Obsidian/releases/tag/Obsidian-v20-20230109). You will need to download a copy before starting. If you are not using Windows, follow the instructions on the `COMPILING.md` file to compile and run the executable.

Tactical Hell provides an Obsidian configuration file, which you can [access here](https://raw.githubusercontent.com/tukkek/tactical-hell/main/CONFIG.txt) (right-click and Save As should work too).

Using Obsidian's `Config Manager`, either click `Load` to open the saved file or copy the configurations to your clipboard manually and then click `Paste`. Either way, to finish, click `Use` to confirm the changes and you can then proceeed to generate your brand-new WAD!

If you don't want to lose your previous settings, `Save` them to a backup file before you do any of the operations here.
