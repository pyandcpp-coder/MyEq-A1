# Autonomous Navigation of TurtleBot3 with ROS 2 Nav2

## Objective

To simulate a TurtleBot3 in a Gazebo environment, create a map of the world using SLAM, and then use the ROS 2 Navigation Stack (Nav2) for autonomous point-to-point navigation.

## My Workflow

My approach was divided into two main phases:

### 1. Mapping
- I launched the `turtlebot3_world` in Gazebo.
- I used the `slam_toolbox` package to begin the SLAM process.
- I manually drove the robot throughout the entire environment using `teleop_key` to build a complete 2D occupancy grid map.
- Once the map was complete, I saved it to `.pgm` and `.yaml` files using the `nav2_map_saver` utility.

### 2. Autonomous Navigation
- With the saved map, I launched the `nav2_bringup` package, providing my custom map as an argument.
- In RViz, I first localized the robot on the map using the "2D Pose Estimate" tool.
- I then sent autonomous navigation commands by setting a "Nav2 Goal", which the robot successfully navigated to while avoiding obstacles.



## Result

# **Demonstration Video:** [Link to Autonomous Navigation Video](https://youtu.be/i6iE2h0CH6g)


## **Screenshot of Navigation:** [Link to Screenshots] (https://github.com/pyandcpp-coder/MyEq-A1/tree/main/media)
 
