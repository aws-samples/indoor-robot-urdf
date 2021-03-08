cmake_minimum_required(VERSION 3.5)
project(robot_description)

find_package(catkin REQUIRED COMPONENTS roslaunch)

catkin_package()

roslaunch_add_file_check(launch)

install(
	DIRECTORY launch  urdf rviz
	DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
	)
