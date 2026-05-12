# <img src="https://raw.githubusercontent.com/llnl/quandary/main/quandary_logo/quandary-logo_logo-inline-color.png" width="512" alt="Quandary"/>

[Quandary](https://github.com/LLNL/quandary) provides optimal control for open and closed quantum systems.

This repository contains example python codes and configurations for Quandary.

# Python examples
See [Quandary](https://github.com/LLNL/quandary) for instructions on running through python.

# Config files
Gate optimization CNOT:
  * Optimizes for a CNOT gate on two coupled qubits each modelled with 2 energy levels. 
  * T = 200ns, time step size = 0.1ns
  * 'cnot.toml': Runs a closed-system (Schroedinger eq.) optimization using random initial control parameters. Can be run on up to 4 cores (one for each initial basis state)
  * 'cnot_FWD_optimized.toml': Evaluates the fidelity of the control parameters stored in 'params_optimized.dat' by forward simulation (Schroedinger's equation)
  * 'cnot_FWD_optimized_withnoise.toml': Same as above, but simulates with Lindblads master equation (with decoherence). 

Gate optimization SWAP02:
  * Considers a qudid modelled with 3 essential energy levels and one guard level
  * Optimizes for a SWAP02 gate that swaps the |0> with the |1> state. 
  * Schroedinger solver (-> closed-system optimization)
  * Can be run on up to 3 compute cores (one for each initial condition)

State-to-state:
  * Optimized for pulses that transfer the ground state of a 2-level qubit with one guard level to the maximally mixed state [1/sqrt(2), 1/sqrt(2)]. 
  * Schroedinger's solver (closed-system optimization)
  * Can run on one core (one initial condition)


# License

Quandary is distributed under the terms of the MIT license. All new contributions must be made under this license. See LICENSE, and NOTICE, for details. 

SPDX-License-Identifier: MIT
