# External Wrench Estimation in Multi-rotor UAVs

Multi-rotor flying robots are increasing their level of autonomy, flying under a variety of conditions, and this forced us to consider real-world situations. This class of robots is subject to local disturbances due to wind effects, collisions, or loss of propellers.
The external wrench (forces and torques) acting on flying robots can be interpreted as a sum of the aerodynamics wrench, the physical interaction wrench, and a fault wrench. Therefore, robust operation under wind influence typically would require additional sensors to discriminate between these constituent wrenches.
In this work we developed a trajectory tracking controller, described in [Simultaneous Contact and Aerodynamic Force Estimation (s-CAFE) for Aerial Robots](https://arxiv.org/abs/1810.12908), to make a quadrotor performing a trajectory tracking task on two path classes: a hovering path and an elliptical path, under the action of external disturbances due to contact and aerodynamic forces. The External Wrench Estimator evaluates the total wrench but is not able to discriminate between interaction and aerodynamic forces, it is implemented in Matlab and it is used to compensate the effect by adding a correction term in the control input. 
 

## Simulation Environment

The project consists of two main modules:

- **Matlab client application**: implements the core logic of the system
 
- **Coppelia simulation scene**: provides the experimental environment and simulation settings


##  Computational Framework

The Matlab application is made up of three main classes:

- **Quadrotor**: implements the dynamic model and properties of the system and provides the control laws for trajectory tracking of the desired task trajectory

- **Aerodynamics**: contains the wrench estimation algorithm and the contact detection procedure

- **QuadrotorSim**: acts as an interface between Matlab logic and Coppelia simulation environment

## Experiments

Two task trajectories are considered: a hovering and an elicoidal trajectory.

We tested the external wrench estimation and contact detection, in the following cases:

- hovering trajectory + impulse force action [video1](https://github.com/FrancescoPeracchia/UAV_External-Wrench-Estimation-in-Multi-rotor-UAVs/blob/main/video/experiment-hovering%2B(down)impulse.mp4) [video2](https://github.com/FrancescoPeracchia/UAV_External-Wrench-Estimation-in-Multi-rotor-UAVs/blob/main/video/experiment-hovering%2B(left)impulse.mp4) [video3](https://github.com/FrancescoPeracchia/UAV_External-Wrench-Estimation-in-Multi-rotor-UAVs/blob/main/video/experiment-hovering%2B(right)impulse.mp4)
- hovering trajectory + wind action [video](https://github.com/FrancescoPeracchia/UAV_External-Wrench-Estimation-in-Multi-rotor-UAVs/blob/main/video/experiment-hovering%2Bwind.mp4)
- hovering trajectory + continuous force action [video](https://github.com/FrancescoPeracchia/UAV_External-Wrench-Estimation-in-Multi-rotor-UAVs/blob/main/video/experiment-hovering%2Bforce.mp4)
- hovering trajectory + wind action + continuous force action [video](https://github.com/FrancescoPeracchia/UAV_External-Wrench-Estimation-in-Multi-rotor-UAVs/blob/main/video/experiment-hovering%2Bwind%26force.mp4)
- hovering trajectory + wind action and not uniformly distributed load mass [video](https://github.com/FrancescoPeracchia/UAV_External-Wrench-Estimation-in-Multi-rotor-UAVs/blob/main/video/experiment-hovering%2Bwind%2Basymmetry.mp4)
- spirale trajectory + wind action [video1](https://github.com/FrancescoPeracchia/UAV_External-Wrench-Estimation-in-Multi-rotor-UAVs/blob/main/video/experiment-spirale%2Bwind%20(1).mp4) [video2](https://github.com/FrancescoPeracchia/UAV_External-Wrench-Estimation-in-Multi-rotor-UAVs/blob/main/video/experiment-spirale%2Bwind%20(2).mp4)

The **force vector** is indicated with a red line while the **wind torque** is indicated with a blue arrow with intensity and direction proportional to its dimension and norm.


## Authors
- [Francesco Starna](https://github.com/Starnino) 
- [Francesco Peracchia](https://github.com/FrancescoPeracchia)
- [Francesco Vincelli](https://github.com/FrancescoVIncelli)

## [Presentation](https://github.com/FrancescoPeracchia/UAV_External-Wrench-Estimation-in-Multi-rotor-UAVs/blob/main/docs/CPR-UAV_Presentation.pdf)
## [Report](https://github.com/FrancescoPeracchia/UAV_External-Wrench-Estimation-in-Multi-rotor-UAVs/blob/main/docs/EiR_UAV_Report.pdf)

## Simulation Example
https://user-images.githubusercontent.com/49724442/161348200-a175f677-54da-4a05-b397-c92ea12cb9fd.mp4

## References
> Teodor Tomić, Philipp Lutz, Korbinian Schmid, Andrew Mathers, Sami Haddadin 2018
[Simultaneous Contact and Aerodynamic Force Estimation (s-CAFE) for Aerial Robots](https://arxiv.org/abs/1810.12908)
