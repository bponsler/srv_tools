cmake_minimum_required(VERSION 2.8.3)
project(tf_tools)

find_package(catkin REQUIRED COMPONENTS tf)

catkin_package()

#catkin_python_setup()

include_directories(${catkin_INCLUDE_DIRS})

add_executable(tf_logger src/tf_logger.cpp)
add_executable(tf_filter src/tf_filter.cpp)
add_executable(apply_tf_to_odom_msg src/apply_tf_to_odom_msg.cpp)

target_link_libraries(tf_logger ${catkin_LIBRARIES})
target_link_libraries(tf_filter ${catkin_LIBRARIES})
target_link_libraries(apply_tf_to_odom_msg ${catkin_LIBRARIES})

