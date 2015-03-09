cmake_minimum_required(VERSION 2.8.11)

project(qt5project)

set(CMAKE_AUTOMOC ON)
set(CMAKE_INCLUDE_CURRENT_DIR ON)

find_package(Qt5Widgets)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${Qt5Widgets_EXECUTABLE_COMPILE_FLAGS}")

set(SOURCE_FILES main.cpp mainwindow.cpp)

add_executable(qt5project ${SOURCE_FILES})
target_link_libraries(${CMAKE_PROJECT_NAME} Qt5::Widgets)
