# hideous_robot
Simulating a hideous wheeled robot in Gazebo for developing/testing point cloud data processing algorithms. 

Install instructions:
Pre: open a new terminal.
1. mkdir -p ~/catkin_ws/src\
Create a new empty directory in your home folder. 
2. cd catkin_ws/src\
Go to the src folder of the new workspace you just created.
3. git clone https://github.com/caffreyu/hideous_robot.git \
Clone this repo to your src folder. 
4. cd .. && catkin_make\
Compile this repo.
5. source devel/setup.bash \
Source the setup file to make the launch files ready for launch commends. 

Using instructions: \
Pre: finish all steps in the install portion. 

For displaying the robot in Gazebo and Rviz:\
Pre: open a new terminal. 
1. roslaunch hideous_robot hideous_world.launch\
This commend will launch the Gazebo simulator, spawm the robot, and show the simulated world in Rviz as well. 

For controlling the robot in the simuated world: \
Pre: open a new terminal.
1. cd catkin_ws/src/hideous_robot/nodes\
Go to the directory where the teleop file is stored. 
2. sudo chmod +x hideous_robot_key_control.py \
Make the control file executable. 
3. rosrun hideous_robot hideous_robot_key_control.py\
Run the controller of the simulated robot.
