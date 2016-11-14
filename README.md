#AGI

This document contains the approach I am taking towards building an AGI system for my reference. I do not have experience in this field, but I am spending my time on it because I want to scratch an itch.

###Basic approach<sup>[1]</sup>:
1. Build a system that can play a game by learning the rules and optimizing for it. The system should be built on proper abstractions and not tied down to the details of the game.
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
3. World: 
    * I'm very unclear about this. The idea is that there if the meta-brain is trying to optimize for it's own health, there has to be a system that affects the health based on the input and output of the brain.

###Architectural components:
1. Client:
    * Connected to a single server, has a range of inputs and actions it can perform.
    * Periodically sends its state and associated meta-data (input, actions and brain version used in the time window) to the server.
    * Receives the brain from the server, which is a plug-and-play module.
    * Client can execute even if connection to server is lost, if it has resolved initial dependancies.
2. Server:
    * Maintains connections with all clients.
    * Stores all info sent by the client.
    * Runs algo against these states to compare performance and modify the executable brain.<sup>[2]</sup> 
    * Pushes updated brain to the clients.

###Current status:
* Modeling the system.
* Defining the learning algo to be run on the server.
* Defining the plug-and-play brain that should be used by the clients.

###Questions:
* How are ideas generated?
* How does a machine build abstractions?

###Notes:
1. Inspired by [DeepMind](https://deepmind.com/).
2. What if the server stores multiple variations of the brain based on the type of input and returns the most appropriate one to the client? Is this a detrimental to the concept of AGI?
