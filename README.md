#AGI

This document contains the approach I am taking towards building an AGI system. I do not have experience in this field, but I am spending my time on it because I want to scratch an itch.

###Basic approach[1]:
1. Build a system that can solve a game by learning the rules and optimizing for it. The system should be built on proper abstractions and not tied down to the details of the game.
2. Use these abstractions for a different scenario. It should not depend on the details of this scenario, other than the type of input and output. 

###Good to have:
* System should not require intense computational resources.
* System should be able to work in a distributed way.
* System should have concept of self. 

###Responsibility of the systems:
1. Brain: 
    * Stores patterns and associated reactions.
    * Match input to pattern and execute.

2. Meta-brain / Consciousness:
    * Measures output quality and biases stored patters accordingly.
    * Hunts for new patterns.
    * Has context of overall system health and tries to optimize for it.
    * Works in the background.

###Questions:
* How are ideas generated?
* How does a machine build abstractions?


###Notes:
1. Inspired by [DeepMind](https://deepmind.com/).

