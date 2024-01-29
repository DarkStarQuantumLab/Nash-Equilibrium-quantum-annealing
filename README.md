# Calculating Nash equilibrium on quantum annealers

Peer-reviewed and published in Annals of Operations Research: https://link.springer.com/article/10.1007/s10479-023-05700-z

Available at: https://www.researchgate.net/publication/377532329_Calculating_Nash_equilibrium_on_quantum_annealers

When diplomats draft international agreements, they are engaged in a strategic game in which they are looking for a **Nash equilibrium**: an agreement from which unilateral deviation by any party will be harmful to the interests of that party. Likewise, when policymakers draft self-policing policies (for example, to mitigate climate change), or financial analysts look for the best market move, they are calculating Nash equilibria. Surprisingly, when birds look for the best nesting grounds during breeding season, they engage in similar strategic games and seek out a Nash equilibrium solution. So ubiquitous is the idea of Nash equilibrium in human activity and nature, and so elegant the mathematical engine that runs it, that its inventor - the mathematician John Nash - was awarded the Nobel prize in economics in 1994.

However, the problem of finding all Nash equilibria in strategic games is a [computationally intensives problem, even in the simple case of two players](https://web.mit.edu/tabbott/Public/final.pdf). While *pure* strategy Nash equilibria can, in principle, be found efficiently, for large games the calculation tends to be infeasible. First generation quantum annealers (from D-Wave Systems) use a first iteration of the promised quantum computational speed up to solve some NP-hard problems faster and with better quality. This project gives a quantum annealing solution to the problem of finding all pure strategy Nash equilibria in two-player, non-cooperative games. When improvements to quantum annealers make real-valued solutions more feasible, this project will extend to include quantum solutions for the problem of finding *mixed* strategy Nash equilibria as well. Finally, extension to multi-player games will be explored.

Nash equilibrium is a two-fold quadratic optimization problem with constraints. This problem was formatted as a single, constrained quadratic optimization in 1964 by Mangasarian and Stone (Two-Person Nonzero-Sum Games and Quadratic Programming). Here, we show that adding penalty terms to the quadratic function formulation of Nash equilibrium gives a quadratic unconstrained binary optimization (QUBO) formulation of this problem that can be executed on quantum annealers. Three examples are discussed to highlight the success of the formulation, and an overall, time-to-solution (hardware + software processing) speed up by seven to ten times is reported on the quantum annealer developed by D-Wave Systems. The quantum annealer was accessed through Amazon Braket, AWS quantum computing service platform. 

The content of this github repository contains the simulation of the examples found in the paper.

You can reproduce the same results by following the instructions given below: 

## Environment Setup

The code has been tested using Python 3.7, 3.8, and 3.9.

The following commandline should install the required packages. It's always good to create a virtual environement to avoid dependencies issues.
```
pip install dwave-ocean-sdk==4.4.0 dwave-neal==0.5.9 amazon-braket-ocean-plugin
```

# Notebooks
The simulated annealing is avaliable [Nash Equilibrium](https://github.com/DarkStarQuantumLab/NashEquilibrium/blob/main/Nash_Equilibrium.ipynb) can be run on Colab and it contains the three examples mentioned in the paper.

The execution on the QPU is avaliable [NE in QPU](https://github.com/DarkStarQuantumLab/NashEquilibrium/blob/main/NE_in_QPU.ipynb)


## Authors
[Olga Okrut](https://github.com/olgOk), [Keith Cannon](https://github.com/krpcannon), [Kareem H. El-Safty](https://github.com/kareem1925), [Nada Elsokkary](https://github.com/NadaElsokkary), [Faisal Shah Khan](https://github.com/FShahKhan)


## How to Cite
If you extend, use this work or the dataset, please cite the [paper](https://arxiv.org/abs/2112.12583) where it was introduced:

```
@article{Olga,
    title={Calculating Nash Equilibrium on Quantum Annealers},
    author={Olga Okrut and Keith Cannon and Kareem H. El-Safty and Nada Elsokkary and Faisal Shah Khan},
    year={2022},
    eprint={2112.12583},
    archivePrefix={arXiv},
    doi = {10.48550/ARXIV.2112.12583},
    primaryClass={cs.GT}
}

```



# License
This work is licensed under the [Apache 2 License](https://www.apache.org/licenses/LICENSE-2.0) and is owned by [Dark Star Quanutm Lab Inc](https://www.darkstarquantumlab.com/)

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
