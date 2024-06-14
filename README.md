Instruction to use this repo to compare trac_ik and kdl for IK problem on your robot in ROS2:
- Clone this repo in your ros2 workspace
- Now in src/trac_ik/trac_ik_examples/launch folder add the urdf of your robot
- Modify line 31 of ur5_arm_launch.py file, write the the name of your urdf file that u added. => "urdf_file = os.path.join(pkg_share, 'launch', '<your_bot_name>.urdf')"
- In line 38 and 39 add the chain_start and chain end link from your urdf and replace it in the default_value
            DeclareLaunchArgument('chain_start', default_value='<eg:base_link>'),
            DeclareLaunchArgument('chain_end', default_value='<eg:wrist_3_link>'),
- Save and build your workspace
- Run the following command to run the test file:
  ros2 launch trac_ik_examples ur5_arm_launch.py 

   
 
