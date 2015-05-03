cmake_minimum_required(VERSION 2.8.3)
project(komodo_gazebo)


find_package(catkin REQUIRED COMPONENTS
  actionlib
  control_msgs
  roscpp
  gazebo_ros
)

catkin_package(
    DEPENDS 
    CATKIN_DEPENDS # TODO
    INCLUDE_DIRS # TODO include
    LIBRARIES # TODO
)


include_directories(include ${catkin_INCLUDE_DIRS})
add_executable(komodo_test_trajectory src/komodo_test_trajectory.cpp)
target_link_libraries(komodo_test_trajectory ${catkin_LIBRARIES})
