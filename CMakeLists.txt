cmake_minimum_required(VERSION 3.22.1)

if(${CMAKE_VERSION} VERSION_LESS 3.22.1)
    cmake_policy(VERSION ${CMAKE_MAJOR_VERSION}.${CMAKE_MINOR_VERSION})
endif()

cmake_policy(SET CMP0048 NEW)

project(UnitConverter VERSION 1.0
    DESCRIPTION "Unit Converter Application made with C++ and Qt"
    LANGUAGES CXX)

find_package(Qt5 COMPONENTS Widgets REQUIRED)

add_executable(${PROJECT_NAME} 
    src/main.cpp
    # mainwindow.ui
    # mainwindow.cpp
    # resources.qrc

)

target_include_directories(${PROJECT_NAME} PRIVATE include)

