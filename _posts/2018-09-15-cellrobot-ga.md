---
layout: post
title: Learning to Adapt Modular Robot Locomotion with CPG-based Hierarchical Control
---

Jiayu Wang, Chuxiong Hu, Yu Zhu


### Abstract
Modular Robots provide high versatility from the ability to reconfigure new morphologies that are better and more efficient for new tasks than conventional robots. However, the design of adaptive and efficient locomotion controllers for arbitrary modular robot structures is challenging. In this paper, we present a two-level hierarchical framework that generates stable rhythmic pattern and automatically learns to quickly and effectively adapt to new situations. Lower level control scheme uses a simplified Central Pattern Generator(CPG) network to produce a stable gait for a given structure of a modular robot, leading to rich locomotion patterns. A neural network as the higher level controller can modulate the parameters of CPG to adapt to new situations and achieve high performance. Here we use simulated robots made of CellRobot modules that have eight mechanical interfaces and one degree of freedom each. This framework is evaluated on multiple locomotion tasks for several robot morphologies in simulation. The results show that our proposed approach can enable robots to adapt the desired trajectory quickly with sample efficiency, and can outperform other state-of-the-art concepts in terms of generalizations capabilities and efficiency.

 
 
![“图片描述”](/images/locomotion.png)

The process of turning locomotion. In this setting, Cellrobot starts at origin at the same time the desired direction is given( red ball). A trained high-level learner can guide the robot to learning to turn correct direction
 
The paper is pre-printed.
