This is the final project of the PDE4420 module.

The main tasks of the project are: 
1. Create a model of the robot
2. Create a map of the environment
3. Scan the map with the robot and determine its localization in it
4. Create a Python program with waiponts to make the robot follow them and avoid obstacles on the map

This project consists of two workspaces:
1. final_project_ws - the main one, with all the main files
2. catkin_make - only with robot model

In addition there is a folder final_maze which contains files of the built maze

To test the project:
1. To start the world and the robot in it, type: 
roslaunch my_final_project my_world.launch

2. To launch gmapping: 
roslaunch my_final_project gmapping.launch

3. To turn on keyboard control: 
rosrun teleop_twist_keyboard teleop_twist_keyboard.py /cmd_vel:=/part2_cmr/cmd_vel

4. To provide a scanned map from the server: 
rosrun map_server map_saver -f ~/final_project_ws/src/my_map

5. To run the AMCL: 
roslaunch my_final_project amcl.launch

6. To start move_base: 
roslaunch my_final_project move_base.launch

7. To start the entire Navigation Stack at once: 
roslaunch my_final_project move_base_demo.launch

8. To run a Python program in which the robot follows waypoints:
roslaunch my_final_project my_world.launch
rosrun my_final_project waypoint.py

Structure of the final_project_ws:
all main files in src

robots_description - model of the robot
my_map - files of the scaned map
my_final_project - all other files of the project
my_final_project/launch - all Navigation Stack files + my_world (launch of the creating maze and robot)
my_final_project/params - params of the move_base
my_final_project/my_map - files of the scanned map
my_final_project/scripts - Python file for following waypoints
my_final_project/world - created world file

final_maze - files of the built maze




