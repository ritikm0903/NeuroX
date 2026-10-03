cmake_minimum_required(VERSION 3.16)
project(NeuroX VERSION 0.1 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

if(NOT CMAKE_BUILD_TYPE)
  set(CMAKE_BUILD_TYPE Release)
endif()

add_executable(hello examples/hello.cpp)
target_include_directories(hello PRIVATE include)
target_compile_options(hello PRIVATE -Wall -Wextra -Wpedantic)
