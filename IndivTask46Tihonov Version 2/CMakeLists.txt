cmake_minimum_required(VERSION 2.8)
set (CMAKE_CXX_STANDARD 11)
enable_language(CXX)
find_package(OpenMP REQUIRED)
set(CMAKE_BUILD_TYPE Release)
set(CMAKE_CXX_FLAGS "-Wall -Wextra")
set(CMAKE_CXX_FLAGS_DEBUG "-g")
set(CMAKE_CXX_FLAGS_RELEASE "-O3")
set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${OpenMP_CXX_FLAGS}")
project(hello_world)
add_executable(main main.cpp)
