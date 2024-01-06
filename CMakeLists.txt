cmake_minimum_required(VERSION 3.10)
project(gauss_newton)

add_compile_options(-std=c++11)

find_package(OpenCV REQUIRED)
include_directories( ${OpenCV_INCLUDE_DIRS} )

add_executable(gauss_newton gauss_newton.cpp)
target_link_libraries(gauss_newton ${OpenCV_LIBS})

install(TARGETS gauss_newton RUNTIME DESTINATION bin)