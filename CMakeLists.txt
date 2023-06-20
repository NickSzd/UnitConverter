cmake_minimum_required(VERSION 3.22.1)

if(${CMAKE_VERSION} VERSION_LESS 3.22.1)
    cmake_policy(VERSION ${CMAKE_MAJOR_VERSION}.${CMAKE_MINOR_VERSION})
endif()

project(UnitConverter VERSION 1.0
    DESCRIPTION "Unit Converter Application made with C++ and Qt"
    LANGUAGES CXX)

cmake_policy(SET CMP0048 NEW)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

find_package(Qt5 CONFIG REQUIRED COMPONENTS Widgets)

add_executable(${PROJECT_NAME} 
    src/main.cpp
    include/mainwindow.ui
    include/mainwindow.cpp
    include/resources.qrc

)
target_link_libraries(${PROJECT_NAME}  Qt5::Widgets)
# target_include_directories(${PROJECT_NAME} PRIVATE include)

