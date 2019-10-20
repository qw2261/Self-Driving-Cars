# Self-Driving Cars Specialization 

## Preview

Be at the forefront of the autonomous driving industry. With market researchers predicting a $42-billion market and more than 20 million self-driving cars on the road by 2025, the next big job boom is right around the corner.

This Specialization gives you a comprehensive understanding of state-of-the-art engineering practices used in the self-driving car industry. You'll get to interact with real data sets from an autonomous vehicle (AV)―all through hands-on projects using the open source simulator CARLA.

Throughout your courses, you’ll hear from industry experts who work at companies like Oxbotica and Zoox as they share insights about autonomous technology and how that is powering job growth within the field.

You’ll learn from a highly realistic driving environment that features 3D pedestrian modelling and environmental conditions. When you complete the Specialization successfully, you’ll be able to build your own self-driving software stack and be ready to apply for jobs in the autonomous vehicle industry.

It is recommended that you have some background in linear algebra, probability, statistics, calculus, physics, control theory, and Python programming. You will need these specifications in order to effectively run the CARLA simulator: Windows 7 64-bit (or later) or Ubuntu 16.04 (or later), Quad-core Intel or AMD processor (2.5 GHz or faster), NVIDIA GeForce 470 GTX or AMD Radeon 6870 HD series card or higher, 8 GB RAM, and OpenGL 3 or greater (for Linux computers).

## Week 1. 

### Module 0: Welcome to the Self-Driving Cars Specialization

**Introduction to Self-driving Cars** 

●  Design a basic hardware system 

●  Identify main components of the autonomous driving software 

●  Create a safety assessment strategy for a self- driving car program 



**State Estimation and Localization** 

●  Understand the key methods for parameter and state estimation 

●  Develop and use models for typical vehicle localization sensors 

●  Apply Kalman filters to a vehicle state estimation problem 

●  Register point clouds from LIDAR to 3D Maps 



**Visual Perception for Self-Driving Cars** 

●  Project 3D points onto the camera image plane 

●  Calibrate the pinhole camera model 

●  Apply feature detection algorithms for localization and mapping 

●  Develop and train neural networks for object detection and semantic segmentation 



**Motion Planning for Self-Driving Cars** 

●  Devise trajectory rollout motion planning 

●  Calculate the time to collision 

●  Define high-level vehicle behaviours 

●  Develop kinematically feasible paths through environments 

●  Compute velocity profiles 



**Specialization Prerequisites**:

●  Proficient in linear algebra 

●  Comfortable with statistics 

●  Comfortable with basic calculus and physics 



#### Welcome to the Course

#### Course Prerequisites

#### Story of Autonomous Vehicles

1925 - Remote Control Car

####Glossary of Terms

ACC: Adaptive Cruise Control

A cruise control system for vehicles which controls longitudinal speed. ACC can maintain a desired reference speed or adjust its speed accordingly to maintain safe driving distances to other vehicles.



Ego

A term to express the notion of self, which is used to refer to the vehicle being controlled autonomously, as opposed to other vehicles or objects in the scene. It is most often used in the form ego-vehicle, meaning the self-vehicle.



FMEA: Failure Mode and Effects Analysis

A bottom up approach of failure analysis which examines individual causes and determines their effects on the higher level system.



GNSS: Global Navigation Satellite System

A generic term for all satellite systems which provide position estimation. The Global Positioning System (GPS) made by the United States is a type of GNSS. Another example is the Russian made GLONASS (Globalnaya Navigazionnaya Sputnikovaya Sistema).



HAZOP: Hazard and Operability Study

A variation of FMEA (Failure Mode and Effects Analysis) which uses guide words to brainstorm over sets of possible failures that can arise.



IMU: Inertial Measurement Unit

A sensor device consisting of an accelerometer and a gyroscope. The IMU is used to measure vehicle acceleration and angular velocity, and its data can be fused with other sensors for state estimation.



LIDAR: Light Detection and Ranging

A type of sensor which detects range by transmitting light and measuring return time and shifts of the reflected signal.



LTI: Linear Time Invariant

A linear system whose dynamics do not change with time. For example, a car using the unicycle model is a LTI system. If the model includes the tires degrading over time (and changing the vehicle dynamics), then the system would no longer be LTI.



LQR: Linear Quadratic Regulation

A method of control utilizing full state feedback. The method seeks to optimize a quadratic cost function dependent on the state and control input.



MPC: Model Predictive Control

A method of control whose control input optimizes a user defined cost function over a finite time horizon. A common form of MPC is finite horizon LQR (linear quadratic regulation).



NHTSA: National Highway Traffic Safety Administration

An agency of the Executive Branch of the U.S. government who has developed a 12-part framework to structure safety assessment for autonomous driving. The framework can be found [here](https://www.nhtsa.gov/sites/nhtsa.dot.gov/files/documents/13069a-ads2.0_090617_v9a_tag.pdf). 



ODD: Operational Design Domain

The set of conditions under which a given system is designed to function. For example, a self driving car can have a control system designed for driving in urban environments, and another for driving on the highway.



OEDR: Object and Event Detection and Response

The ability to detect objects and events that immediately affect the driving task, and to react to them appropriately.



PID: Proportional Integral Derivative Control

A common method of control defined by 3 gains.

1) A proportional gain which scales the control output based on the amount of the error

2) An integral gain which scales the control output based on the amount of accumulated error

3) A derivative gain which scales the control output based on the error rate of change



RADAR: Radio Detection And Ranging

A type of sensor which detects range and movement by transmitting radio waves and measuring return time and shifts of the reflected signal.



SONAR: Sound Navigation And Ranging

A type of sensor which detects range and movement by transmitting sound waves and measuring return time and shifts of the reflected signal.



### Meet the Self-Driving Car Experts

Steven Waslander

Jonathan Kelly

Diana, Zoox

Winston, Zoox

Andy, Zoox

Paul Newman, Oxbotica

### Module 1. Autonomy Requirements

### Lesson 1. Taxonomy of Driving

Terms and Definitions 

- Driving task
  - Perceiving the environment
  - Planning how to reach from point A to point B ○ Controlling the vehicle 
- Operational Design Domain (ODD) 



How to classify driving system automation? 

- Driver attention requirements 
- Driver action requirements 
- What exactly makes up a driving task? 
  - **Lateral control** - steering 
  - **Longitudinal control** - braking, accelerating
  - **Object and Event Detection and Response** (OEDR): detection, reaction
  - **planning** 
    - long term (route) 
    - short term 
  - **miscellaneous** 



Level 0 - No Automation 

Level 1 - Driving Assistance 

- **Adaptive Cruise Control**
  - can control speed, driver has to steer 
- **Lane Keeping Assistance**
  - can help you stay in your lane, if you drift 

 Level 2 - Partial Driving Automation 

- GM Super Cruise 
- Nissan ProPilot Assist 

Level 3 - Conditional Driving Automation 

- Lateral Control, Longitudinal Control, OEDR
- Includes automated object and event detection and response 

Level 4 - High Driving Automation 

- Lateral Control, Longitudinal Control, OEDR, Fallback
- Handles emergencies autonomously, driver can entirely focus on other tasks. 

Level 5 - Full Driving Automation 

- Lateral Control, Longitudinal Control, OEDR, Fallback, Unlimited ODD



Limitations of this taxonomy

- ODD and safety record are more important! 



Supplementary Reading: Taxonomy of Driving

You may download the SAE J3016: Taxonomy and Definitions Document that was referenced in the Lesson 1 video lecture on the SAE website: https://www.sae.org/standards/content/j3016_201806/.

You can also check out other freely available information about the Taxonomy of Driving on [SAE’s website](https://www.sae.org/).



### Lesson 2. **Requirements for Perception** 

![](/Users/wangqi/Desktop/Courses/2019下半年/Self-Driving-Cars/Lectures/Week_1/assets/1.png)

What is perception?

- We want to make sense of the environment and ourselves 

- Two things:
  - identification 
  - understanding motion 
- Why?
  - to inform our driving decisions 



Goal for perception

- Static objects
  - Road and lane markings (on-road) 
  - Curbs (off-road)
  - Traffic lights (off-road) 
  - Road signs (off-road) 
  - Construction signs, obstructions, and more (on-road) 
-  Dynamic objects (on-road) 
  - Vehicles 
    - 4 wheelers (cars, trucks ...) 
    - 2 wheelers (motorbikes, bicycles, ...) 
  - Pedestrians 
- Ego localization 
  - Position 
  - Velocity, acceleration
  - Orientation, angular motion 



Challenges to perception 

- Robust detection and segmentation 
- Sensor uncertainty
- Occlusion, reflection
- Illumination, lens flare 
- Weather, precipitation 



Supplementary Reading: Requirements for Perception

To learn more about the KITTI Vision Benchmark Suite, check out this link: http://www.cvlibs.net/datasets/kitti



### Lesson 3. Driving Decisions and Actions 

Planning: Examples 

- Making decisions 
  - Long term
    - How to navigate from New York to Los Angeles? 
  - Short term
    - Can I change my lane to the lane right of me?
    - Can I pass this intersection and join the left road? 
  - Immediate
    - Can I stay on track on this curved road? 
    - Accelerate or brake, by how much? 

- Rule Based Planning (reactive planning)
  - What we just did was rule based planning
    - Involved decision tree
  - In reactive rule based planning, we have rules that take into accont the current state of ego and other objects and give decisions
  - Examples:
    - If there is a pedestrain on the road, stop
    - If speed limit changes, adjust speed to march it
- What other types of planning are there? 
  - Predictive Planning: 
    - Make predictions about other vehicles and how they are moving. Then use these predictions to inform our decisions
    - Example: 
      - That car has been stopped for the last 10 seconds. It is going to be stopped for the next few seconds
      - Pedestrian is jaywalking. She will enter our lane by the time we reach her



Supplementary Reading: Driving Decisions and Actions

If you're curious about motion planning and other high-level behaviour, check out [Frazzioli’s Survey for Autonomous Planning](https://arxiv.org/pdf/1604.07446.pdf).

This paper, [Autonomous driving in urban environments: Boss and the Urban Challenge](https://onlinelibrary.wiley.com/doi/epdf/10.1002/rob.20255); discusses one of the very early mixed planning systems. It was also the winner of the DARPA Urban Challenge

