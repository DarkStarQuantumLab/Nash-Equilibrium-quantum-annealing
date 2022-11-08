# Calculating Nash equilibrium on quantum annealers

When politicians look to make international agreements, whether they realize it or not, they are engaged in a strategic game in which they are looking for a **Nash equilibrium**: an agreement from which unilateral deviation by any party will be harmful to the interests of that party. Likewise, when birds look for the best nesting grounds during breeding season, they engage in similar strategic games and seek out a Nash equilibrium solution. So ubiquitous is the idea of Nash equilibrium in human activity and nature, and so elegant the mathematical engine that runs it, that its inventor - the mathematician John Nash - was awarded the Nobel prize in economics in 1994.

However, the problem of finding all Nash equilibrium in strategic games is NP-hard, even in the simple case of two palyers (see https://web.mit.edu/tabbott/Public/final.pdf, page 4). First generation quantun annealers (from D-Wave Systems) use the promised quantum computational speed up to solve some NP-hard problems faster. This project gives a quantum annealing solution to the problem of finding all *pure* trategy Nash equilibria in two-player, non-cooperative games. When improvements to quantum annealers make real-valued solutions feasible, this project will extend to inlclude quantum computing solution for the problem of finding *mixed* strategy Nash equilibria as well. 

Nash equilibrium is a two-fold quadratic optimization problem with constraints. This problem was formatted as a single, constrained quadratic optimization in 1964 by Mangasarian and Stone (Two-Person Nonzero-Sum Games and Quadratic Programming). Here, we show that adding penalty terms to the quadratic function formulation of Nash equilibrium gives a quadratic unconstrained binary optimization (QUBO) formulation of this problem that can be executed on quantum annealers. Three examples are discussed to highlight the success of the formulation, and an overall, time-to-solution (hardware + software processing) speed up by seven to ten times is reported on the quantum annealer developed by D-Wave Systems. The quantum annealer was accessed through Amazon Braket, AWS quantum computing service platform. 

(PDF) Calculating Nash Equilibrium on Quantum Annealers. Available from: https://www.researchgate.net/publication/360264494_Calculating_Nash_Equilibrium_on_Quantum_Annealers [accessed Nov 06 2022].

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
