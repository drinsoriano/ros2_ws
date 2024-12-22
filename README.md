Project Overview

ROS2 workspace that integrates:

DDSM115: Controlled via RS485 for motor control without encoder feedback.
LiDAR: For mapping and obstacle detection (e.g., RPLIDAR or Hokuyo).
Nav2 (Navigation2): For path planning and navigation.
Since the motor lacks encoders, odometry will be approximated using motor speed commands and supplemented with LiDAR and/or IMU data.


Directory Structure

~/ros2_ws/
├── src/
│   ├── ddsm115_driver/               # Custom ROS2 package for DDSM115 motor control
│   │   ├── ddsm115_driver/
│   │   │   ├── __init__.py
│   │   │   ├── ddsm115_driver.py     # ROS2 node for controlling DDSM115
│   │   │   ├── odometry_publisher.py # Odometry estimation logic
│   │   │   └── __main__.py
│   │   ├── package.xml
│   │   └── setup.py
│   ├── lidar_driver/                 # LiDAR driver (e.g., RPLIDAR or Hokuyo)
│   │   └── (Installed via apt or custom driver)
│   ├── nav2_config/                  # Configuration for Navigation2
│   │   ├── launch/
│   │   │   └── nav2_bringup.launch.py
│   │   └── config/
│   │       └── nav2_params.yaml
│   ├── rplidar_ros/                  # Installed LiDAR package
│   └── (Other ROS2 packages as needed)
