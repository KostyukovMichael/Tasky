cmake_minimum_required(VERSION 3.20.0)
project(Tasky VERSION 0.1.0 LANGUAGES C CXX)

set(SOURCES main.cpp)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++20 -Wall")

add_executable(Tasky ${SOURCES})

find_package(nlohmann_json REQUIRED)
target_link_directories(Tasky PRIVATE nlohmann_json::nlohmann_json)