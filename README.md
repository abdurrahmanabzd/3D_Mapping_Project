# 3D Mapping Project
**(Please read the note in the end before downloading project files)**

In this project a 2D occupancy grid and 3D octomap were created from a simulated environment using a robot with the RTAB-Map package. In this project the *rtabmap_ros* package was used, which is a ROS wrapper (API) for interacting with RTAB-Map. 

RTAB-Map (Real-Time Appearance-Based Mapping) is a popular solution for SLAM to develop robots that can map environments in 3D. RTAB-Map has good speed and memory management, and it provides custom developed tools for information analysis. (documentation: http://wiki.ros.org/rtabmap_ros)

*ROS Teleop Package* is needed to navigate the robot in the environment. (download link: https://github.com/ros-teleop/teleop_twist_keyboard)

To run the project:
- (new terminal) $ roslaunch my_robot world.launch
- (new terminal) $ rosrun teleop_twist_keyboard teleop_twist_keyboard.py
- (new terminal) $ roslaunch my_robot mapping.launch

Whenever mapping is done, use the *rtabmap-databaseViewer* for complete analysis of the mapping session. To do so; Run on terminal:
- $ rtabmap-databaseViewer ~/.ros/rtabmap.db

Once open, add some windows to get a better view of the relevant information:
- Say yes to using the database parameters
- View -> Constraint View
- View -> Graph View

*localization.launch* file is for using the map generated for localization. 

***NOTE: The package name is originally "my_robot". Make sure to name the package "my_robot" instead of "3D_Mapping_Project" after cloning the files before executing catkin_make. Otherwise, errors may occur.***
