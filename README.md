## A Status and BlockScience Collaboration 
### Economic Model Research, Simulation, and Testing

### Architecture Digest
[Contextual hierarchy](Status_Digest_1_Architecture.pdf) of the STATUS network as a cryptoeconomic system.

### Cooperative Behavior Digest
[Incentive Mechanism](Status_Digest_2_Cooperative_Behavior.pdf) underlying the p2p network.

### Models and Tests
Implementing the above architecture and design decisions into models reside in branches in this repository. 

#### Validation Model
[Network Routing Model](https://github.com/status-im/storage-econ-model/tree/validation_model) validating networkx objects as class within simulation for retaining activity and dynamic local connectivity information.

#### OVerlay Network Model
Building off the validation model, adding [Kademlia Ping and Store RPC methods](https://github.com/status-im/storage-econ-model/tree/ijkp_kdf) for maintaining node neighborhood activity and liveness logs.

#### Online Learning Incentive Model
An [online learning incentive model](https://github.com/status-im/storage-econ-model/tree/subsidy_tax_tuning) provides sudsidies and charges penalties for incentivizing faster routing. A series of experiments explores the parametric tuning of the classifier as well as the amount of message payment subject to penalty and available for subsidy.

#### Payment Distribution Testing
Experiments allocating payemnt percentages for proscribed tasks necessary for [message routing](https://github.com/status-im/storage-econ-model/tree/route_allocation_test) and [message storage](https://github.com/status-im/storage-econ-model/tree/storage_allocation_test). Both sets of parametric tests explore the economic fabric of the network as nodes take on blended tasks to operate the network through the concept of personas.

#### Escrow Relaxation
Moving away from necessitating escrowed payment prior to message initiation to allow for [cooperative behavior](https://github.com/status-im/storage-econ-model/tree/escrow_relaxation) in a decentralized manner. 

Simulations and tests were performed using cadCAD.

#### To explore for yourself, you must install Python 3 and our Python package ***cadCAD*** .
```
                    __________   ____
  ________ __ _____/ ____/   |  / __ \
 / ___/ __` / __  / /   / /| | / / / /
/ /__/ /_/ / /_/ / /___/ ___ |/ /_/ /
\___/\__,_/\__,_/\____/_/  |_/_____/
by BlockScience
======================================
       Complex Adaptive Dynamics       
       o       i        e
       m       d        s
       p       e        i
       u       d        g
       t                n
       e
       r
```
***cadCAD*** is a Python package that assists in the processes of designing, testing and validating complex systems through simulation, with support for Monte Carlo methods, A/B testing and parameter sweeping. 

# Getting Started with cadCAD
## 0. Pre-installation Virtual Environments with [`venv`](https://docs.python.org/3/library/venv.html) (Optional):
If you wish to create an easy to use virtual environment to install cadCAD inside of, please use the built in `venv` package.

***Create** a virtual environment:*
```bash
$ python3 -m venv ~/cadcad
```

***Activate** an existing virtual environment:*
```bash
$ source ~/cadcad/bin/activate
(cadcad) $
```

***Deactivate** virtual environment:*
```bash
(cadcad) $ deactivate
$
```

## 1. Installation: 
Requires [>= Python 3.6](https://www.python.org/downloads/) 

**Option A: Install Using [pip](https://pypi.org/project/cadCAD/)** 
```bash
$ pip3 install cadCAD
```

**Option B:** Build From Source
```
$ pip3 install -r requirements.txt
$ python3 setup.py sdist bdist_wheel
$ pip3 install dist/*.whl
```

**Option C: Using [Nix](https://nixos.org/nix/)**
1. Run `curl -L https://nixos.org/nix/install | sh` or install Nix via system package manager
2. Run `nix-shell` to enter into a development environment, `nix-build` to build project from source, and 
`nix-env -if default.nix` to install

The above steps will enter you into a Nix development environment, with all package requirements for development of and 
with cadCAD. 

This works with just about all Unix systems as well as MacOS, for pure reproducible builds that don't 
affect your local environment.

## 2. Documentation:
* [Simulation Configuration](documentation/README.md)
* [Simulation Execution](documentation/Simulation_Execution.md)
* [Policy Aggregation](documentation/Policy_Aggregation.md)
* [Parameter Sweep](documentation/System_Model_Parameter_Sweep.md)
* [Display System Model Configurations](documentation/System_Configuration.md)

## 3. Connect:
Find other cadCAD users at our [Discourse](https://community.cadcad.org/). We are a small but rapidly growing community.

## 4. [Contribute!](CONTRIBUTING.md)

## 5. Install Dependent Data Science Libraries
```
   $ pip3 install numpy
   $ pip3 install pandas
   $ pip3 install networkx
   $ pip3 install scipy
   $ pip3 install matplotlib
   $ pip3 install seaborn
```
