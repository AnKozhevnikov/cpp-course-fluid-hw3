cmake_minimum_required(VERSION 3.8)
project(Fluid)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS}")

add_executable(fast fluid_fast.cpp ThreadPool.hpp)
target_compile_options(fast PRIVATE -O0)

add_executable(original fluid_original.cpp)
target_compile_options(original PRIVATE -O0)