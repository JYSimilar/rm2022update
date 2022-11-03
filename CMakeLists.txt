cmake_minimum_required(VERSION 3.23)
project(rm2022)

set(CMAKE_CXX_STANDARD 20)

find_package(OpenCV)
include_directories(${OpenCV_INCLUDE_DIRS})


add_executable(rm2022
        include/rgb.h
        lib/rgb.cpp
        lib/main.cpp
        lib/Solution.cpp
        include/Solution.h
        include/armor_detector.h
        include/Kalman.h
        include/SolvePnP.h
        lib/armor_detector.cpp
        lib/Kalman.cpp
        lib/SolvePnP.cpp
        lib/armor_tracker.cpp
        include/armor_tracker.h
        )
target_link_libraries(rm2022 ${OpenCV_LIBS})