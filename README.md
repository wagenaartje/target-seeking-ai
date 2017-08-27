# Target-seeking AI
This repository shows how you can use [Neataptic](https://github.com/wagenaartje/neataptic) to succesfully teach neural networks to trace targets. You can see the genomes live in action [here](https://wagenaartje.github.io/target-seeking-ai/). These genomes have been trained for over 100 generations and are very effective. Visualisation done with [P5.js](https://p5js.org/). The next step would be adding collisions, to possibly reveal some interesting tactics.

[Read an article on this repo here](https://wagenaartje.github.io/neataptic/articles/targetseeking/).

These forks of this library are interesting to check out as well:

* [corpr8's fork](https://corpr8.github.io/neataptic-targetseeking-tron/)
gives each neural agent its own acceleration, as well as letting each arrow
remain in the same place after each generation. This creates a much more
'fluid' process.

## Settings
If you manage to optimize the settings, please perform either a pull request or create an issue [here](https://github.com/wagenaartje/neataptic/issues). 

#### Settings (contained in `js/main.js`):
* `WIDTH` set the width of the playing field
* `HEIGHT` set the height of the playing field
* `MAX_SPEED` set the maximal multiplier speed a genome can have (smaller genomes move faster)
* `START_X` set the x-location from which each genome (and the target) starts
* `START_Y` set the y-location from which each genome (and the target) starts
* `SCORE_RADIUS` set the distance to the target from where genomes get assigned score
* `PLAYER_AMOUNT` set the amount of genomes that play on the field (population size)
* `ITERATIONS` set the amount of iterations/frames each generation is tested for
* `START_HIDDEN_SIZE` set the amount of hidden nodes each genome starts witch
* `MUTATION_RATE` set the mutation rate
* `ELITISM` set the amount of elitism

Most important setting:
* `USE_TRAINED_POP` setting this to `false` will start the evolution from scratch (USE THIS WHEN OPTIMIZING THE SETTINGS), setting this to `true` will use the pre-trained population

#### Default setting values
```javascript
var WIDTH            = $('#field').width();
var HEIGHT           = 800;
var MAX_SPEED        = 5;
var START_X          = WIDTH/2;
var START_Y          = HEIGHT/2;
var SCORE_RADIUS     = 100;

// GA settings
var PLAYER_AMOUNT    = Math.round(2.3e-4 * WIDTH * HEIGHT);
var ITERATIONS       = 250;
var MUTATION_RATE    = 0.3;
var ELITISM          = Math.round(0.1 * PLAYER_AMOUNT);

// Trained population
var USE_TRAINED_POP = true;
```
