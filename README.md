This project focuses on optimizing energy distribution in a smart grid system using Genetic Algorithms (GA) and Python’s multiprocessing for parallel computation. It simulates a 24-hour energy distribution cycle across grid nodes and sources, evaluating performance, cost, and efficiency under both serial and parallel modes.
# Project Overview
The objective of this project is to design an intelligent, scalable optimization solution for smart energy distribution. The Genetic Algorithm dynamically evolves optimal allocation strategies under various constraints such as cost, demand, and supply availability. Parallel processing is leveraged to reduce execution time during fitness evaluations
# Features

-  Genetic Algorithm implementation for smart grid optimization
-  Multiprocessing-based parallel fitness evaluation
-  Simulation of 10 Grid Nodes and 3 Energy Sources
-  24-Hour optimization cycle simulation
-  CPU & GPU usage monitoring (using `psutil` and `GPUtil`)
-  Execution time benchmarking between Serial and Parallel modes
-  Baseline greedy model for comparison

# Technologies Used

- Python 3.x  
- NumPy  
- Matplotlib  
- Multiprocessing (built-in)  
- Psutil (for CPU monitoring)  
- GPUtil (for GPU monitoring)

# Dataset Description

- 10 Grid Nodes  
  - Demand range: 50–150 MW  
  - Max capacity: 200 MW  
  - Transmission loss: 5–15%
  
- 3 Energy Sources
  - Supply range: 300–500 MW  
  - Cost per MW: 5–15 units  
  - Availability: 80%–100%

- 24-Hour Simulation
  - The GA runs every simulated hour to reflect dynamic grid behavior.

##Performance Summary

| Mode     | Average Time (24 Hours) | CPU Usage | Speedup |
|----------|--------------------------|------------|---------|
| Serial   | 0.07 seconds             | ~12%       | 1×      |
| Parallel | 1.54 seconds             | ~96%       | 0.05×   |

Note: In this lightweight simulation, multiprocessing added overhead and was slower than serial mode. However, parallelism is highly beneficial in larger, more complex scenarios.


