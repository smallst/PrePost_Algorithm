cmake_minimum_required(VERSION 2.6)
project(cpp)

set(CMAKE_CXX_COMPILER "g++")
set(CMAKE_CXX_FLAGS "-fPIC -g -Wall -O3 -std=c++11")
#set(CMAKE_CXX_FLAGS_RELEASE "-fPIC -Wall -std=c++11 -O3")
## if you use opencv,uncomment next line
# find_package(OpenCV REQUIRED)

aux_source_directory(${PROJECT_SOURCE_DIR}/src SRC_LIST)

## if you want use subdirectory for some function
## uncomment next line and add directory name to last line,the same as opencv
# add_subdirectory(src/astar)

# include_directories(/usr/local/Aria/include)
# include_directories(/usr/local/Aria/ArNetworking/include)
include_directories(${PROJECT_SOURCE_DIR}/include)
# link_directories(/usr/local/Aria/lib)

## replace demo.cpp with your own main.cpp
add_executable(cpptest ${SRC_LIST})

# target_link_libraries(robottest Aria pthread dl rt astar ${OpenCV_LIBS})
