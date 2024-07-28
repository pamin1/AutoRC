# AutoRC
This is my project based off the F1/10th competition. I intend on competing at the 2025 ICRA Conference in Atlanta;
however, I am primarily using this as a learning experience for Computer Vision and Robotics.

## Setup
I am using the ARRMA Senton 4X4 vehicle platform, with an Nvidia Jetson for my onboard compute.
In addition, there is a PX4 FCU + PDB to interface the Jetson and vehicle hardware together.

For my sensors I am using the Intel Realsense D455 camera and the built in IMU for VIO purposes.
My goal is to eventually have VSLAM capabilities for this vehicle moving forward.

## Current Progress 
So far I have made progress into developing offboard control of the vehicle using the QGroundControl ground station
to utilize the PX4. The end goal of offboard control is to prove that we are able to take continous input data,
process it, and instruct the car to move accordingly. Continous imaging and processing will be done through the D455
and an Apriltag. Ideally, the vehicle will be able to acceleration and steering to follow an apriltag.

This will be done as a precursory step to implementing VIO and VSLAM.