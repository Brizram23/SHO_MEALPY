# SELFISH HERD OPTIMIZER (SHO)

Python implementation of the **Selfish Herd Optimizer (SHO)** using the **MEALPY optimization framework**.

---

## Overview

The **Selfish Herd Optimizer (SHO)** is a population-based metaheuristic algorithm inspired by the behavior of selfish herds in nature under predation risk.

In this model, individuals attempt to reduce their probability of being attacked by predators by positioning themselves relative to other members of the herd.

The optimization algorithm models two groups of agents:

* Herd members (prey)
* Predators

During the optimization process, the following mechanisms occur:

* Herd members move according to leadership and social interaction rules.
* Predators pursue weaker herd members.
* A predation phase removes weak individuals from the population.
* A restoration phase generates new individuals from surviving herd members.

These mechanisms allow the algorithm to balance:

* **Exploration of the search space**
* **Exploitation of promising solutions**

---

## Reference Paper

Fausto, F., Cuevas, E., Valdivia, A., & González, A.

**A Global Optimization Algorithm Inspired in the Behavior of Selfish Herds**

BioSystems, Volume 160, Pages 39–55, 2017

DOI  
https://doi.org/10.1016/j.biosystems.2017.07.010

---

## Brief Summary

The Selfish Herd Optimizer models predator–prey interactions within a population of candidate solutions.

Each individual receives a **survival value**, which determines its influence during the search process.

The algorithm follows several stages:

1. Population initialization
2. Division into herd members and predators
3. Herd movement phase
4. Predator movement phase
5. Fitness evaluation
6. Predation phase
7. Herd restoration phase
8. Global memory update

This process helps maintain diversity while guiding the population toward optimal regions of the search space.

---

## Requirements

Install the required dependencies:

```
pip install numpy mealpy
```

---

## Project Structure

Example repository structure:

```
project/
│
├── sho.py
│   Implementation of the Selfish Herd Optimizer
│
├── run_ackley.py
│   Example experiment using the Ackley benchmark function
│
└── README.md
```

---

## Example Objective Function

The following example uses the **Ackley benchmark function**, a well-known multimodal function commonly used to evaluate optimization algorithms.

## Performance Metrics

The following statistical indicators are used to evaluate the algorithm performance.

| Metric | Description |
|------|-------------|
| **AB** | Average best fitness across runs |
| **MB** | Median best fitness across runs |
| **SD** | Standard deviation of the results |

These metrics help evaluate both **accuracy** and **stability** of the optimization algorithm.

---

## Typical Parameter Settings

Recommended parameters:

* Population size: **50**
* Maximum iterations: **1000**
* Herd ratio: **random value between 0.7 and 0.9**

---

## Reproducibility

Each independent run uses a fixed random seed:

```
seed = i
```

This allows the experiments to be **reproducible and comparable**.

---

## Suggested Citation

If you use this implementation in academic research, please cite the following article:

```
@article{fausto2017sho,
title={A global optimization algorithm inspired in the behavior of selfish herds},
author={Fausto, Fernando and Cuevas, Erik and Valdivia, Arturo and González, Adrián},
journal={BioSystems},
volume={160},
pages={39--55},
year={2017},
publisher={Elsevier},
doi={10.1016/j.biosystems.2017.07.010}
}
```

---

## License

This implementation is provided for **research and educational purposes**.
