# pygrnd

is a libary of various quantum algorithms written by the Team JoS QUANTUM GmbH to support the development of Applications for quantum computing in Finance, Insurance and Energy.

The Asset Allocator is an example to optimize a financial porfolio's overall variance depending of the covariance of the assets.
The example shows how the problem is mathematically translated as a quadratic unconstrainted binary optimization ('QUBO'). This models is equivalent to the Ising model which can be mapped and solved by quantum annealer from e.g. D-Wave, variational quantum algorithms like VQE and QAOA on gate-based universal quantum computers or quantum-inspired solver.

## Setup

Pre-required: pygrnd
https://github.com/JoSQUANTUM/pygrnd

pip install tqdm
pip install numpy
pip install dimod
pip install greedy

## usage

Application: Create Market neutral portfolio

-> Pick stocks from a list of assets (here we provided an example covariance matrix from the German DAX 30 index)

-> We want to pick 5 long and 5 short positions

-> We want minimal variance -> similar to constraint

-> Minimizing variance with a QUBO is straightforward

-> Use covariance matrix as Q

The functions construct the QUBO matrix including the constraints for total budget (constraint 1: Q_c1) and long and short positions (constraint 2: Q_c2).



