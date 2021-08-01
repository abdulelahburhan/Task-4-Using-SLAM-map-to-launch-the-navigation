# Task-4-Using-SLAM-map-to-launch-the-navigation
Previously the task didn't work so I didn't upload it then I did it again and it worked i followed the [E-manual](https://emanual.robotis.com/docs/en/platform/turtlebot3/navigation/#navigation) 
# Steps for launching the navigation
 1. first we lunch the similated world by typing
  
  `$ export TURTLEBOT3_MODEL=burger` \
   `$ roslaunch turtlebot3_gazebo turtlebot3_world.launch` 
   
   We know that from the [previous-task](https://github.com/abdulelahburhan/Task-2-Using-Turtlebot3-with-SLAM-approach-to-create-and-save-a-map) and the [similation E-manual](https://emanual.robotis.com/docs/en/platform/turtlebot3/simulation/) 
   ![124306665-60fd5500-db6f-11eb-97ad-644a0609e6db](https://user-images.githubusercontent.com/85543378/127769557-7c07460a-762f-4f89-9018-9d8b2d28da89.JPG)
  ![124306699-6d81ad80-db6f-11eb-9200-dc83e671f22a](https://user-images.githubusercontent.com/85543378/127769560-3ebbb89a-fde2-436b-aad4-9b378714aa9e.JPG)

Both simulation runned successfully

 2.  Then we need to Launch the Navigation
     from a new terminal with `CTRL` + `Alt` + `T`
     We type these codes in it
     
    `$ export TURTLEBOT3_MODEL=burger` \
    `$ roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml` 
    
   ![Capture](https://user-images.githubusercontent.com/85543378/127769749-17e3aaf1-1173-4a0d-bd80-36b16bed2857.JPG)
   
Navigation runned successfully

  3.Estimating Initial Pose
 
 [DISCLAIMER] Initial Pose Estimation must be performed before running the Navigation
 
 3.1.Click the 2D Pose Estimate button in the RViz menu.
 
 ![2d_pose_button](https://user-images.githubusercontent.com/85543378/127769961-ccb67b26-f126-486b-b031-6215ee95fbc0.png)

3.2.Click on the map where the actual robot is located and drag the large green arrow toward the direction where the robot is facing.

3.3.Repeat step 1 and 2 until the LDS sensor data is overlayed on the saved map.

3.4.Launch keyboard teleoperation node to precisely locate the robot on the map using.

  `$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch`
3.5.Move the robot back and forth a bit to collect the surrounding environment information and narrow down the estimated location of the TurtleBot3 on the map which is displayed with tiny green arrows.
3.6.Terminate the keyboard teleoperation node by entering `ctrl` + `C`

  4.Set Navigation Goal
 4.1.Click the 2D Nav Goal button in the RViz menu.
 4.2.Click on the map to set the destination of the robot and drag the purple arrow toward the direction where the robot will be facing.
 ![ezgif-3-ec0e7fa16284](https://user-images.githubusercontent.com/85543378/127770312-caababbb-9681-4ca8-ac02-aa454de07877.gif)
