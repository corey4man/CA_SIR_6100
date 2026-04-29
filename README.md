# CA_SIR_6100
## Credit: Alexander Burnham

Link to Driver Code: [ca_sir_driver](ca_sir_driver.html)

## How This SIR Model Works:

### Agent-Based SIR Model Using Cellular Automata

This simulation implements an agent-based SIR (Susceptible-Infected-Recovered) model on a 2D grid, similar to a cellular automaton (CA). Each grid cell represents an individual in one of three states:

Susceptible (S): Healthy, can become infected.


Infected (I): Currently infectious, can transmit disease to neighbors.


Recovered (R): Immune and no longer infectious.


Neighborhood: Each cell interacts with its 8 surrounding neighbors (Moore neighborhood). The number of infected neighbors determines the probability of a susceptible cell becoming infected.

### Rules and Probabilities:

Infection: A susceptible cell becomes infected with probability `1 - (1 - β)^n`, where β is the infection probability per neighbor, and n is the number of infected neighbors.
Recovery: An infected cell recovers with probability γ per time step.


### User Interaction:

Left click → infect a susceptible cell.

Right click → make a cell recovered.

Spacebar → toggle automatic simulation.

S key → single-step the simulation.

C key → reset the grid.

Over time, the simulation tracks the proportion of S, I, and R individuals and plots their dynamics, illustrating epidemic spread patterns.