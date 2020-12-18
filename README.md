# OreoPanc4ke's Artifact Sub Rater
https://twitch.tv/oreopanc4kes

This is a quick and jank modified version of the original [Genshin Artifact Rater](https://github.com/shrubin/Genshin-Artifact-Rater) for personal use. Original README [here](https://github.com/shrubin/Genshin-Artifact-Rater/blob/master/README.md).

Changed it to only rate substat rolls on how well they rolled compared to the max possible roll. Main stats are excluded - just use a piece with the right main stat 4Head what's the point of rating it if it's the wrong one?

Substat rolls are rated against the max number of perfect rolls for the level it's at (4 starting +1 per 4 levels for a max of 9 at +20). Provides both unweighted and weighted numbers, as well as uses a less opinionated default weighting that values ER% and EM at full, since both are very valuable if you need them (sometimes better than ATK/CR/CDMG).

Users can then just interpret the numbers in whatever context they're using that piece for. 

#### Default Weights

ATK%, CR%, CDMG%, EM, ER% - 1 \
Flat ATK - 0.4 (based on a reasonable 800 base atk) \
Everything else - 0

## Usage

```
-rate <image/url> [<stat>=<weight> ...]
```

#### Weights
Set custom weights (valued between 0 and 1)
```
-rate atk=1 er=0 atk%=0.5
```
\<stat> is any of hp, hp%, atk, atk%, er, em, cr, cd, def, def%
