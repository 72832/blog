---
title:  "Motion Profiling"
categories: 
  - Advanced
last_modified_at: 2019-02-22T08:06:00-05:00
---

<img src="https://github.com/AtsushiSakai/PythonRobotics/raw/master/icon.png?raw=true" align="right" width="300"/>

# Migrated from PythonRobotics
### AtsushiSakai/PythonRobotics

Python codes for robotics algorithm.

# What is this?

This is a Python code collection of robotics algorithms, especially for autonomous navigation.

Features:

1. Easy to read for understanding each algorithm's basic idea.

2. Widely used and practical algorithms are selected.

3. Minimum dependency.

See this paper for more details:

- [\[1808\.10703\] PythonRobotics: a Python code collection of robotics algorithms](https://arxiv.org/abs/1808.10703) ([BibTeX](https://github.com/AtsushiSakai/PythonRoboticsPaper/blob/master/python_robotics.bib))

# Requirements

- Python 3.6.x (2.7 is not supported)

- numpy

- scipy

- matplotlib

- pandas

- [cvxpy](http://www.cvxpy.org/en/latest/) 

# Documentation

This README only shows some examples of this project. 

If you are interested in other examples or mathematical backgrounds of each algorithm, 

You can check the full documentation online: [https://pythonrobotics.readthedocs.io/](https://pythonrobotics.readthedocs.io/)

All animation gifs are stored here: [AtsushiSakai/PythonRoboticsGifs: Animation gifs of PythonRobotics](https://github.com/AtsushiSakai/PythonRoboticsGifs)


# Localization

## Extended Kalman Filter localization

<img src="https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/Localization/extended_kalman_filter/animation.gif" width="640">

Documentation: [Notebook](https://github.com/AtsushiSakai/PythonRobotics/blob/master/Localization/extended_kalman_filter/extended_kalman_filter_localization.ipynb)

## Particle filter localization

![2](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/Localization/particle_filter/animation.gif)

This is a sensor fusion localization with Particle Filter(PF).

The blue line is true trajectory, the black line is dead reckoning trajectory,

and the red line is estimated trajectory with PF.

It is assumed that the robot can measure a distance from landmarks (RFID).

This measurements are used for PF localization.

Ref:

- [PROBABILISTIC ROBOTICS](http://www.probabilistic-robotics.org/)


## Histogram filter localization

![3](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/Localization/histogram_filter/animation.gif)

This is a 2D localization example with Histogram filter.

The red cross is true position, black points are RFID positions.

The blue grid shows a position probability of histogram filter.  

In this simulation, x,y are unknown, yaw is known.

The filter integrates speed input and range observations from RFID for localization.

Initial position is not needed.

Ref:

- [PROBABILISTIC ROBOTICS](http://www.probabilistic-robotics.org/)

# Mapping

## Gaussian grid map

This is a 2D Gaussian grid mapping example.

![2](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/Mapping/gaussian_grid_map/animation.gif)

## Ray casting grid map

This is a 2D ray casting grid mapping example.

![2](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/Mapping/raycasting_grid_map/animation.gif)

## k-means object clustering

This is a 2D object clustering with k-means algorithm.

![2](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/Mapping/kmeans_clustering/animation.gif)

## Rectangle fitting

This is a 2D rectangle fitting for vehicle detection.

![2](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/Mapping/rectangle_fitting/animation.gif)


# SLAM

Simultaneous Localization and Mapping(SLAM) examples

## Iterative Closest Point (ICP) Matching

This is a 2D ICP matching example with singular value decomposition.

It can calculate a rotation matrix and a translation vector between points to points.

![3](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/SLAM/iterative_closest_point/animation.gif)

Ref:

- [Introduction to Mobile Robotics: Iterative Closest Point Algorithm](https://cs.gmu.edu/~kosecka/cs685/cs685-icp.pdf)


## FastSLAM 1.0

This is a feature based SLAM example using FastSLAM 1.0.

The blue line is ground truth, the black line is dead reckoning, the red line is the estimated trajectory with FastSLAM.

The red points are particles of FastSLAM.

Black points are landmarks, blue crosses are estimated landmark positions by FastSLAM.


![3](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/SLAM/FastSLAM1/animation.gif)


Ref:

- [PROBABILISTIC ROBOTICS](http://www.probabilistic-robotics.org/)

- [SLAM simulations by Tim Bailey](http://www-personal.acfr.usyd.edu.au/tbailey/software/slam_simulations.htm)


## Graph based SLAM

This is a graph based SLAM example.

The blue line is ground truth.

The black line is dead reckoning.

The red line is the estimated trajectory with Graph based SLAM.

The black stars are landmarks for graph edge generation.

![3](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/SLAM/GraphBasedSLAM/animation.gif)

Ref:

- [A Tutorial on Graph-Based SLAM](http://www2.informatik.uni-freiburg.de/~stachnis/pdf/grisetti10titsmag.pdf)


# Path Planning

## Dynamic Window Approach

This is a 2D navigation sample code with Dynamic Window Approach.

- [The Dynamic Window Approach to Collision Avoidance](https://www.ri.cmu.edu/pub_files/pub1/fox_dieter_1997_1/fox_dieter_1997_1.pdf)

![2](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/PathPlanning/DynamicWindowApproach/animation.gif)


## Grid based search

### Dijkstra algorithm

This is a 2D grid based shortest path planning with Dijkstra's algorithm.

![PythonRobotics/figure_1.png at master · AtsushiSakai/PythonRobotics](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/PathPlanning/Dijkstra/animation.gif)

In the animation, cyan points are searched nodes.

### A\* algorithm

This is a 2D grid based shortest path planning with A star algorithm.

![PythonRobotics/figure_1.png at master · AtsushiSakai/PythonRobotics](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/PathPlanning/AStar/animation.gif)

In the animation, cyan points are searched nodes.

Its heuristic is 2D Euclid distance.

### Potential Field algorithm

This is a 2D grid based path planning with Potential Field algorithm.

![PotentialField](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/PathPlanning/PotentialFieldPlanning/animation.gif)

In the animation, the blue heat map shows potential value on each grid.

Ref:

- [Robotic Motion Planning:Potential Functions](https://www.cs.cmu.edu/~motionplanning/lecture/Chap4-Potential-Field_howie.pdf)

## State Lattice Planning

This script is a path planning code with state lattice planning.

This code uses the model predictive trajectory generator to solve boundary problem.

Ref: 

- [Optimal rough terrain trajectory generation for wheeled mobile robots](http://journals.sagepub.com/doi/pdf/10.1177/0278364906075328)

- [State Space Sampling of Feasible Motions for High-Performance Mobile Robot Navigation in Complex Environments](http://www.frc.ri.cmu.edu/~alonzo/pubs/papers/JFR_08_SS_Sampling.pdf)


### Biased polar sampling

![PythonRobotics/figure_1.png at master · AtsushiSakai/PythonRobotics](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/PathPlanning/StateLatticePlanner/BiasedPolarSampling.gif)


### Lane sampling

![PythonRobotics/figure_1.png at master · AtsushiSakai/PythonRobotics](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/PathPlanning/StateLatticePlanner/LaneSampling.gif)

## Probabilistic Road-Map (PRM) planning 

![PRM](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/PathPlanning/ProbabilisticRoadMap/animation.gif)

This PRM planner uses Dijkstra method for graph search.

In the animation, blue points are sampled points,

Cyan crosses means searched points with Dijkstra method,

The red line is the final path of PRM.

Ref:

- [Probabilistic roadmap \- Wikipedia](https://en.wikipedia.org/wiki/Probabilistic_roadmap)

　　

## Rapidly-Exploring Random Trees (RRT)

### RRT\*

![PythonRobotics/figure_1.png at master · AtsushiSakai/PythonRobotics](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/PathPlanning/RRTstar/animation.gif)

This is a path planning code with RRT\*

Black circles are obstacles, green line is a searched tree, red crosses are start and goal positions.

Ref:

- [Incremental Sampling-based Algorithms for Optimal Motion Planning](https://arxiv.org/abs/1005.0416)

- [Sampling-based Algorithms for Optimal Motion Planning](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.419.5503&rep=rep1&type=pdf)

### RRT\* with reeds-sheep path

![Robotics/animation.gif at master · AtsushiSakai/PythonRobotics](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/PathPlanning/RRTStarReedsShepp/animation.gif))

Path planning for a car robot with RRT\* and reeds sheep path planner.

### LQR-RRT\*

This is a path planning simulation with LQR-RRT\*.

A double integrator motion model is used for LQR local planner.

![LQRRRT](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/PathPlanning/LQRRRTStar/animation.gif)

Ref:

- [LQR\-RRT\*: Optimal Sampling\-Based Motion Planning with Automatically Derived Extension Heuristics](http://lis.csail.mit.edu/pubs/perez-icra12.pdf)

- [MahanFathi/LQR\-RRTstar: LQR\-RRT\* method is used for random motion planning of a simple pendulum in its phase plot](https://github.com/MahanFathi/LQR-RRTstar)


## Quintic polynomials planning

Motion planning with quintic polynomials.

![2](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/PathPlanning/QuinticPolynomialsPlanner/animation.gif)

It can calculate 2D path, velocity, and acceleration profile based on quintic polynomials.

Ref:

- [Local Path Planning And Motion Control For Agv In Positioning](http://ieeexplore.ieee.org/document/637936/)

## Reeds Shepp planning

A sample code with Reeds Shepp path planning.

![RSPlanning](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/PathPlanning/ReedsSheppPath/animation.gif?raw=true)

Ref:

- [15.3.2 Reeds\-Shepp Curves](http://planning.cs.uiuc.edu/node822.html) 

- [optimal paths for a car that goes both forwards and backwards](https://pdfs.semanticscholar.org/932e/c495b1d0018fd59dee12a0bf74434fac7af4.pdf)

- [ghliu/pyReedsShepp: Implementation of Reeds Shepp curve\.](https://github.com/ghliu/pyReedsShepp)


## LQR based path planning

A sample code using LQR based path planning for double integrator model.

![RSPlanning](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/PathPlanning/LQRPlanner/animation.gif?raw=true)


## Optimal Trajectory in a Frenet Frame 

![3](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/PathPlanning/FrenetOptimalTrajectory/animation.gif)

This is optimal trajectory generation in a Frenet Frame.

The cyan line is the target course and black crosses are obstacles.

The red line is predicted path.

Ref:

- [Optimal Trajectory Generation for Dynamic Street Scenarios in a Frenet Frame](https://www.researchgate.net/profile/Moritz_Werling/publication/224156269_Optimal_Trajectory_Generation_for_Dynamic_Street_Scenarios_in_a_Frenet_Frame/links/54f749df0cf210398e9277af.pdf)

- [Optimal trajectory generation for dynamic street scenarios in a Frenet Frame](https://www.youtube.com/watch?v=Cj6tAQe7UCY)


# Path Tracking

## move to a pose control

This is a simulation of moving to a pose control

![2](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/PathTracking/move_to_pose/animation.gif)

Ref:

- [P. I. Corke, "Robotics, Vision and Control" \| SpringerLink p102](https://link.springer.com/book/10.1007/978-3-642-20144-8)


## Stanley control

Path tracking simulation with Stanley steering control and PID speed control.

![2](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/PathTracking/stanley_controller/animation.gif)

Ref:

- [Stanley: The robot that won the DARPA grand challenge](http://robots.stanford.edu/papers/thrun.stanley05.pdf)

- [Automatic Steering Methods for Autonomous Automobile Path Tracking](https://www.ri.cmu.edu/pub_files/2009/2/Automatic_Steering_Methods_for_Autonomous_Automobile_Path_Tracking.pdf)



## Rear wheel feedback control

Path tracking simulation with rear wheel feedback steering control and PID speed control.

![PythonRobotics/figure_1.png at master · AtsushiSakai/PythonRobotics](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/PathTracking/rear_wheel_feedback/animation.gif)

Ref:

- [A Survey of Motion Planning and Control Techniques for Self-driving Urban Vehicles](https://arxiv.org/abs/1604.07446)


## Linear–quadratic regulator (LQR) speed and steering control

Path tracking simulation with LQR speed and steering control.

![3](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/PathTracking/lqr_speed_steer_control/animation.gif)

Ref:

- [Towards fully autonomous driving: Systems and algorithms \- IEEE Conference Publication](http://ieeexplore.ieee.org/document/5940562/)


## Model predictive speed and steering control

Path tracking simulation with iterative linear model predictive speed and steering control.

<img src="https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/PathTracking/model_predictive_speed_and_steer_control/animation.gif" width="640">

Ref:

- [notebook](https://github.com/AtsushiSakai/PythonRobotics/blob/master/PathTracking/model_predictive_speed_and_steer_control/Model_predictive_speed_and_steering_control.ipynb)

## Nonlinear Model predictive control with C-GMRES

A motion planning and path tracking simulation with NMPC of C-GMRES 

![3](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/PathTracking/cgmres_nmpc/animation.gif)

Ref:

- [notebook](https://github.com/AtsushiSakai/PythonRobotics/blob/master/PathTracking/cgmres_nmpc/cgmres_nmpc.ipynb)


# Arm Navigation

## N joint arm to point control

N joint arm to a point control simulation.

This is a interactive simulation.

You can set the goal position of the end effector with left-click on the ploting area. 

![3](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/ArmNavigation/n_joint_arm_to_point_control/animation.gif)

In this simulation N = 10, however, you can change it.

## Arm navigation with obstacle avoidance 

Arm navigation with obstacle avoidance simulation.

![3](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/ArmNavigation/arm_obstacle_navigation/animation.gif)


# Aerial Navigation

## drone 3d trajectory following 

This is a 3d trajectory following simulation for a quadrotor.

![3](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/AerialNavigation/drone_3d_trajectory_following/animation.gif)

## rocket powered landing

This is a 3d trajectory generation simulation for a rocket powered landing.

![3](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/AerialNavigation/rocket_powered_landing/animation.gif)

Ref:

- [notebook](https://github.com/AtsushiSakai/PythonRobotics/blob/master/AerialNavigation/rocket_powered_landing/rocket_powered_landing.ipynb)

# Bipedal

## bipedal planner with inverted pendulum

This is a bipedal planner for modifying footsteps with inverted pendulum.

You can set the footsteps and the planner will modify those automatically.

![3](https://github.com/AtsushiSakai/PythonRoboticsGifs/raw/master/Bipedal/bipedal_planner/animation.gif)

# License 

MIT

# Use-case

See: [users\_comments](https://github.com/AtsushiSakai/PythonRobotics/blob/master/users_comments.md)

# Contribution

A small PR like bug fix is welcome.

If your PR is merged multiple times, I will add your account to the author list.

Your comment using [![Say Thanks!](https://img.shields.io/badge/Say%20Thanks-!-1EAEDB.svg)](https://saythanks.io/to/AtsushiSakai) is also welcome. 

This is a list: [Users comments](https://github.com/AtsushiSakai/PythonRobotics/blob/master/users_comments.md)

# Authors

- [Atsushi Sakai](https://github.com/AtsushiSakai/) ([@Atsushi_twi](https://twitter.com/Atsushi_twi))

- [Daniel Ingram](https://github.com/daniel-s-ingram)

- [Joe Dinius](https://github.com/jwdinius)

- [Karan Chawla](https://github.com/karanchawla)

- [Antonin RAFFIN](https://github.com/araffin)

- [Alexis Paques](https://github.com/AlexisTM)

