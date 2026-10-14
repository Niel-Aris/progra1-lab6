cmake_minimum_required(VERSION 3.16)
project(Lab6 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)

find_package(Qt6 REQUIRED COMPONENTS Widgets)

add_executable(Lab6
    main.cpp
    Lab6.cpp
    Lab6.h
    Lab6.ui
)

set_target_properties(Lab6 PROPERTIES
    OUTPUT_NAME "Qt Widgets"
    MACOSX_BUNDLE TRUE
    MACOSX_BUNDLE_BUNDLE_NAME "Qt Widgets"
    MACOSX_BUNDLE_GUI_IDENTIFIER "com.carlossoto.progra1-lab6"
)

target_link_libraries(Lab6 PRIVATE Qt6::Widgets)
