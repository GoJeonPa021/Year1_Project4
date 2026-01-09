# Year1_Project4
# Cellular Automata Traffic Flow Simulation

This project explores the application of **Cellular Automata (CA)** models to urban traffic flow, specifically comparing car-only traffic with mixed traffic containing both cars and buses.

## Project Overview
The simulation evaluates dynamic traffic flow using a simplified cellular automata model implemented in Python. The primary goal is to determine how vehicle density and the ratio of cars to buses affect the average speed and passenger throughput of a road network.


## Key Features
* **Discrete Grid Modeling**: The road is divided into cells that are either empty (0) or occupied by a car (1) or bus (2).
* **Mixed Vehicle Dynamics**:
    * **Cars**: Occupy 1 cell and require 1 empty space in front to move.
    * **Buses**: Require 2 empty spaces in front to move, representing their larger physical footprint and movement constraints.
* **Periodic Boundaries**: Simulations use a circular road model where vehicles exiting the "end" wrap around to the "start" to maintain a constant number of vehicles.
* **Passenger Efficiency Analysis**: Investigates the optimal vehicle mix to transport 500 passengers across a 100-cell space.


## Movement Rules
The simulation follows a specific iterative ruleset based on established CA traffic models:
1. **Check Movement**: All cars attempt to move 1 step and all buses attempt to move 2 steps.
2. **Condition Check**: A car moves if the next cell is empty; a bus moves if the next two cells are empty.
3. **Speed Calculation**: The instantaneous speed is calculated as the ratio of actual movement to total available space.
4. **Iteration**: The process repeats until the speed reaches a constant steady state.

## Results & Optimization
* **Car-Only Model**: In a 10-cell system, maximum speed (0.5) is achieved when there are 5 cars; beyond this density, speed decreases as the road becomes congested.
* **Bus Integration**: Increasing the number of buses relative to cars generally increases the total passenger speed, as buses hold 6x the capacity of a car (30 vs 5 passengers) while only requiring one additional empty cell to move.
* **Optimization Goal**: To transport 500 passengers at a speed of at least 0.9 on a 100
