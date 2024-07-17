# STEPS FOR INSTALLING NEW VERSION OF BEHAVIORTREE.ROS2 PACKAGE 

1) Go to the directory u want to put this package, then: \
	`git clone https://github.com/BehaviorTree/BehaviorTree.ROS2.git`

2) Then go to your VScode and open terminal. Type in: \
	`pip install jinja2
	pip install typeguard`

4) Then git clone generate_parameter_library in the same directory: \
	`git clone https://github.com/PickNikRobotics/RSL.git](https://github.com/PickNikRobotics/generate_parameter_library.git`

5) Then git clone RSL in the same directory: \
	`git clone https://github.com/PickNikRobotics/RSL.git`
	
6) Git clone the cpp_polyfills folder: \
	`https://github.com/PickNikRobotics/cpp_polyfills.git`

7) After that, if don't want to do the: \
	`export CMAKE_PREFIX_PATH=/path/to/tcb_span:$CMAKE_PREFIX_PATH` \
   then do: \
   	`extract the "tcb_span" and "tl_expected" files out from cpp_polyfills into the same
   	directory as your behaviortree_ros2 packages`
   	
8) Do colcon build and you are basically done. Unless you want to use the btcpp_ros2_samples plugin (sleep_client_dyn), in which case you would need to change the path to either of the following:

	`install/btcpp_ros2_samples/share/btcpp_ros2_samples/bt_plugins/libsleep_plugin.so` \
						OR \
	`install/btcpp_ros2_samples/lib/btcpp_ros2_samples/libsleep_plugin.so"`
