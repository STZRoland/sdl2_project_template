cmake_minimum_required(VERSION 3.16)
project(MySDL2App)

# Find the SDL2 library
find_package(SDL2 REQUIRED)

# Add the SDL2 include directory to the include path
include_directories(${SDL2_INCLUDE_DIRS})

# Set up the build
add_executable(MySDL2App main.cpp)
target_link_libraries(MySDL2App ${SDL2_LIBRARIES})

# Set C++ standard and other options
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)