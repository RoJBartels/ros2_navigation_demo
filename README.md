# Autonomous Navigation with ROS2 (TurtleBot3)

## Overview

This project demonstrates a complete autonomous navigation pipeline using ROS2 and TurtleBot3 in simulation.

The robot is capable of:

* Building a map using SLAM
* Localizing itself within the map
* Planning a path to a target
* Navigating autonomously

---

## Tech Stack

* ROS2 (Humble)
* TurtleBot3
* Gazebo
* Cartographer (SLAM)
* Nav2 (Navigation)

---

## Features

* 2D SLAM with Lidar
* Occupancy grid map generation
* Autonomous navigation using Nav2
* Goal-based path planning

---

## Demo

(Add screenshots or video here)

---

## How to Run

### 1. Start Simulation

```bash
ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py
```

### 2. Run SLAM

```bash
ros2 launch turtlebot3_cartographer cartographer.launch.py use_sim_time:=true
```

### 3. Save Map

```bash
ros2 run nav2_map_server map_saver_cli -f ~/map
```

### 4. Run Navigation

```bash
ros2 launch turtlebot3_navigation2 navigation2.launch.py use_sim_time:=true map:=<path_to_map.yaml>
```

---

## Result

The robot successfully navigates autonomously to user-defined goals in a simulated environment.

---

## Future Improvements

* Real robot deployment
* Obstacle avoidance tuning
* Multi-room mapping
