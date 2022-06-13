# EE346-Final-Lab
This is the lab resources for SUSTech EE346 2022 final lab.

# Usage

## 1. Clone the source code
  sudo apt-get install ros-melodic-navigation
  
  cd ~/catkin_ws/src
  
  git clone https://github.com/tf1423079696/EE346-final-lab.git
  
## 2. Catkin make the EE346-lab6 package
  cd ..
  
  catkin_make

## 3. Add course models to the end of ~/.bashrc in computer(replace 192.168.3.244 as your comuter ip)
   export TURTLEBOT3_MODEL=burger
   
   export ROS_MASTER_URI=http://192.168.3.244:11311
   
   export ROS_HOSTNAME=192.168.3.244
   
## 4. Add course models to the end of ~/.bashrc in your robot(replace 192.168.3.244 as your comuter ip,192.168.3.81 as your robot ip)
   export ROS_MASTER_URI=http://192.168.3.244:11311
   
   export ROS_HOSTNAME=192.168.3.81

## 5. Source the .bashrc file(in both computer and robot)
   source ~/.bashrc
   
## 6. Connect your robot(replace 192.168.3.81 as your robot ip)
   roscore 
   
   in a new  terminal: ssh pi@192.168.3.81
   
   roslaunch turtlebot3_bringup turtlebot3_robot.launch
   
## 7. Run the project
   
   To run the navigation node, you need to first move "map.pgm" (or "map_new.pgm") and "map.yaml" (or "map_new.yaml") from /maps to /home directory ("map.pgm" and "map.yaml" are map files with lower accuracy, while "map_new.pgm" and "map_new.yaml" with higher accuracy). However, we use "map.pgm" and "map.yaml" in the final lab.
   
   cd ~/catkin_ws/src/EE346-final-lab/
   
   roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml
   
   In a new terminal:
   
   cd ~/catkin_ws/src/EE346-final-lab/
   
   rosrun sound_play soundplay_node.py
   
   In a new terminal:
   
   cd ~/catkin_ws/src/EE346-final-lab/scripts
   
   python final_run.py 

## 8. Stop the robot
   cd ~/catkin_ws/src/EE346-final-lab/scripts
   
   python lane_following_reset.py 

   
 
   


