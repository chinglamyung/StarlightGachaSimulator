# GachaSimulator
For analysis in the mobile game called "Revue Starlight Relive!"

Provided is a Jupyter Notebook.
Gacha has a pity mechanic, where every 100 rolls without getting a 4-star rarity stage girl, you are guaranteed to get a random 4* stage girl (weighted toward the featured character). This simulation automatically tries to manipulate the pity system whenever the opportunity presents itself to improve the average gem spent.
Run the cells to generate the histogram for each unique banner types, e.g. birthday banners, collab banners, troupe-revue support banners, etc.

For the spotlight banner, change hyperparameters to most closely match real-world data collected.
The model used for spotlight banner is a weighted system (i.e. as long as any non-excellent prizes remain, the probability to get an excellent prize stays the same and is unchanged.

SPOTLIGHT GACHA DETAILS:

Each step contains two components: first, the player performs a normal 10x pull, with 0.2% to obtain the featured girl per roll (so ten chances at 0.2% success each). Then, the player is granted a prize from a bingo board of 9 slots. If 3 excellent prizes are obtained, then the bingo board moves onto set #2. Set #2 has two slots with the featured girl guaranteed.
The featured girl is, however, not guaranteed in the stage girl slot of bingo set#1. Rather, she has a 40% chance to appear if that particular excellent prize is obtained.

Step 1 thru 3 are discounted in gem cost, and are thus irrelevant to the simulation.
Step 4 guarantees an excellent prize from the bingo prize pool. (does not matter if in set#1 or set#2)
