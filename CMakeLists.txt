# Minimum version of CMake required to build this project
cmake_minimum_required(VERSION 3.0)

# Name of the project
project(RoadableSurfaceLocator)

set(SRC_DIR src)

# Add all the source files needed to build the executable
add_executable(
  RoadableSurfaceLocator
  src/main.cpp
  #${SRC_DIR}/Person.cpp
)

# Include the directory where MyLibrary project is. Otherwise, we can't use the
# library
# add_subdirectory(libraries/MyLibrary)

find_package (Eigen3 3.3 REQUIRED)

# Link the executable and the library together
add_subdirectory(vendors/pcl)