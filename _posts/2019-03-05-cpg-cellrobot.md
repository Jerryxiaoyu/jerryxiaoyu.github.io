---
layout: post
title: CPG-based Hierarchical Control for Quadrupedal Locomotion Using Deep Reinforcement Learnin
---

Jiayu Wang, Chuxiong Hu, Yu Zhu

### Abstract
Legged robots have the potential to exhibit an unmatched ability to perform versatile and robust locomotion. However, the design of effective and adaptive locomotion controllers for arbitrary legged morphologies is challenging.
In this paper, we present a novel hierarchical learning framework for a central pattern generator (CPG)-based quadruped locomotion using deep reinforcement learning.
The proposed method can be used to learn robust locomotion policies capable of walking different patterns while accomplishing user-specified tasks. By injecting user commands into inputs, we can train a neural network to guide the CPG-based controller online to follow the desired motion by modulating the optimized parameters of the CPG controller. The architecture allows the robot to leverage and combine (i) CPG oscillators to generate rhythmic gaits, and (ii) neural networks to explore a black-box map from states and commands to CPG parameters.
The framework is employed on a modular robot, CellRobot and compared with hand-engineered methods to evaluate the effectiveness and robustness. The simulation demonstrates that using the learned policies the quadruped achieves locomotion skills: straight walking, velocity tracking, and circular turning. The results suggest that the learning framework is also capable of robustly adapting to new conditions.

![“图片描述”](/images/system_whole.svg)

Hierarchical locomotion learning framework. In a upper-level locomotion policy, the network maps the current observations and user commands to a 2-dimension latent vector. The lower-level CPG controller takes in the two latent factors and utilizes them to modulate the parameters of left side (blue) and right side (yellow), respectively. Finally the CPG controller outputs the joint position targets, which can be servoed by a PD controller to generate joint toques. In the CPG controller, the latent factor $z_{l}$ and $z_{r}$ are used to modulate parameters of the oscillators belonging to the left front (LF) and left hind leg(LH), and the ones of oscillators belonging to the right front (HF) and right hind leg(RH).

![“图片描述”](/images/vel_whole.svg)

Quantitative evaluation of the learned locomotion controller in velocity tracking tasks.
(A and B) Base velocity tracking and corresponding base position tracking the performance of the learned policy with random commands. The desired position trajectory is computed by integrating the desired velocities.
(C and D) Comparison of the learned controller against the hand-crafted PID controller, in terms of the root-mean-square of the position errors (C) and velocity error(D), given forward velocity commands of 0.05, 0.10, 0.15, and 0.20 m/s and a random initial state of the robot.
(E) The produced gait pattern for 0.15m/s forward velocity command.
LF, left front leg; RF, right front leg; LH, left hind leg; RH, right hind leg.
 
![“图片描述”](/images/turning_trajectories.svg)

Trajectories of the base with different desired radius R_d in an episode (20 seconds). The robot starts walking at (0, 0) in the direction of the positive X-axis.

 
 
The paper is pre-printed and is under review.