cmake_minimum_required(VERSION 2.8)
project( DisplayImage )
find_package( OpenCV REQUIRED )
set (CMAKE_CXX_STANDARD 11)
include_directories( ${OpenCV_INCLUDE_DIRS} )
add_executable( DisplayImage src/DisplayImage.cpp )
target_link_libraries( DisplayImage ${OpenCV_LIBS} )