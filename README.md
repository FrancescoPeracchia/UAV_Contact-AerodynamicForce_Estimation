# External Wrench Estimation in Multi-rotor UAVs

Project for the first module of the Electives in Robotics / Control Problems in Robotics exam at Sapienza University of Rome.


An External Wrench Estimator is proposed, this algorithm is described in 'Simultaneous Contact and Aerodynamic Force Estimation (s-CAFE) for Aerial Robots' ![paper](https://arxiv.org/abs/1810.12908), the estimator is implemented in Matlab and the Estimated External Wrench is used to compensate the effect by adding a correction term in the control input. 
 

## Simulation Environment

The project consists of two main modules:

 the Matlab client application, implementing the core logic of the system
 
 the Coppelia simulation scene, providing the experimental environment and simulation settings


##  Computational Framework

The Matlab application is made up of three main classes:

- Quadrotor : implements the system dynamics and provides the control design for tracking task

- Aerodynamics : contains the wrench estimation algorithm and the contact detection procedure

- QuadrotorSim : acts as an interface between Matlab logic and Coppelia simulation environment

## Experiments

Two task trajectories are considered: a hovering and an elicoidal trajectory.

We tested the external wrench estimation and contact detection, in the following cases:


- in presence of wind action only
- in presence of a continuous contact action but in absence of wind action
- in presence of a continuous contact action and of wind action
- in presence of wind action and not uniformly distributed load mass


Francesco Starna 
Francesco Peracchia 
Francesco Vincelli


https://user-images.githubusercontent.com/49724442/161348200-a175f677-54da-4a05-b397-c92ea12cb9fd.mp4





