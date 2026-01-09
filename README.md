# Year1_Project4
# Cellular Automata Traffic Flow Simulation README

This project explores the application of **Cellular Automata (CA)** models to urban traffic flow, specifically comparing car-only traffic with mixed traffic containing both cars and buses.

## Project Overview

The simulation evaluates dynamic traffic flow using a simplified cellular automata model implemented in Python. The primary goal is to determine how vehicle density and the ratio of cars to buses affect the average speed of a road network.

## Key Features

* 
**Discrete Grid Modeling**: The road is divided into cells that are either empty or occupied by at most one vehicle.


* **Mixed Vehicle Dynamics**:
* 
**Cars**: Occupy 1 cell and require 1 empty space in front to move.


* 
**Buses**: Occupy 1 cell but require 2 empty spaces in front to move, representing their larger physical footprint.




* 
**Periodic Boundaries**: Simulations use a circular road model where vehicles exiting the "end" wrap around to the "start".


* 
**Efficiency Analysis**: Investigates the optimal vehicle mix to transport 500 passengers across a 100-cell space.



## Movement Rules

The simulation follows a specific iterative ruleset:

1. 
**Step 1**: Define potential movement (1 step for cars, 2 steps for buses).


2. 
**Step 2**: Check if the required leading cells are empty (0).


3. 
**Step 3**: Calculate instantaneous speed as (total movement / total space).


4. 
**Step 4**: Repeat iterations until the average speed reaches a constant state.



## Results & Optimization

* 
**Car Model**: Maximum speed (0.5) in a 10-cell system is achieved with exactly 5 cars.


* 
**Bus Integration**: Data supports the hypothesis that increasing the ratio of buses to cars increases overall transport speed for a fixed passenger count.


* 
**Passenger Goal**: To transport 500 passengers at a speed of at least 0.9, a minimum of 11 buses is required.



## Implementation Requirements

* 
**Language**: Python 3.x 


* **Libraries**: `numpy`, `matplotlib`

## References

* Nagel, K., & Schreckenberg, M. (1992). A cellular automaton model for freeway traffic.


* Benjamin, Johnson, and Hui (1996). BJH model.


* Fukui M. and Ishibashi Y. (1996).
