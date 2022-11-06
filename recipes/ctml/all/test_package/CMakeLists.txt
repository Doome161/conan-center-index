cmake_minimum_required(VERSION 3.8)
project(test_package LANGUAGES CXX) # if the project uses c++

find_package(CTML REQUIRED CONFIG)

add_executable(${PROJECT_NAME} test_package.cpp)
target_link_libraries(${PROJECT_NAME} PRIVATE CTML::CTML)
target_compile_features(${PROJECT_NAME} PRIVATE cxx_std_11)
