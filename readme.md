Doucmentation for MIC Mini Project:
Author: Jordan Smith

Definition:
A Petri net is defined as a triple (P, T, F) where:
● P is a finite set of places
● T is a finite set of transitions (P ∩ T = ∅)
● F ⊆ (P x T) ∪ (T x P) is a set of arcs (flow relation) {for short we will write f(p→t) to
describe an arc that connect transition t to place p}
Additionally, marking M ∈ P → Z* is a function that assigns a non-negative integer to every
place and represents the state of the net (some definitions call this a marked petri net). M(p)
denotes the marking of place p. Inplaces of a transition (*t) is a set of places where each
element of a set is connected to the transition (the place is the source of the arc and the
transition is the destination). Conversely, outplaces of a transition (t*) is a set of places that are
connected to the transition by arcs where the places are the destinations and the transition is
the source.
The following definitions cover how the petri net progress from one marking to another:
● t ∈ T is enabled if ∀ p ∈ P | ∃ f(p→t) ∈ F M(p) > 0 - for all inplaces of the transition
(that are connected to the transition via an incoming arc) the amount of tokens at the
place is non zero
● Firing an enabled transition decreases the amount of tokens on all inplaces with one and
increases the amount of token in all outplaces of the transition by one.

Domain:
So the domain of this project focuses on the use of petri nets. For the design of the Petri Net, I chose to use something of a theme park approach. I am an avid enjoyer of
theme parks, so I just simply chose to approach designing my particular petri net domain/example in that of a theme park, the domain consists of PetriNode Objects,
transitions and arcs -> because of the way I approached the model, because I am a little unfamiliar with webgme and am not too familiar with the syntax and how to make
the state machine and the simulator more efficient unfortunately I did have to kind of adapt with the little time that I had in order to make it work. With that being
said my "simulator" is basically not existent so I essentially tried to automate the petri net with code. In order to use my domain you will simply need to draw out the
model that you are trying to solve, from there you will then need to instantiate each petri net with its appropriate name, capacity and starting size, followed
by each transition with its name, and each arc with it's associated weight and attached petri nodes, from there you will need to go through and add each arc to the appropriate
PetriNode and Transition. Once everything is connected and you have the model set up then you can simply call the start_state_machine function and it will iterate through each
PetriNode until it reaches a finished state after so many loops or the code will crash out if it becomes deadlocked.

Installation:
Since I used the web version of webgme you would simply only need to use it via mic.isis.vanerbilt.edu
