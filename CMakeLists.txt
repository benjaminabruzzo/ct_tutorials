cmake_minimum_required(VERSION 2.8.3)
project(my_ct_project)
add_compile_options(-std=c++11)

find_package(catkin REQUIRED COMPONENTS
  ct_core
  ct_models
  ct_optcon
  ct_rbd
  roscpp
)

catkin_package(
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

add_executable(main src/main.cpp)
	target_link_libraries(main ${catkin_LIBRARIES})

add_executable(masspoint src/masspoint.cpp)
	target_link_libraries(masspoint ${catkin_LIBRARIES})
