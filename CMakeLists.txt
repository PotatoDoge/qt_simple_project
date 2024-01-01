cmake_minimum_required(VERSION 3.26)
project(qt_simple_project)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

set(CMAKE_PREFIX_PATH "/opt/homebrew/Cellar/qt@5/5.15.11")

find_package(Qt5 COMPONENTS
        Core
        Gui
        Widgets
        REQUIRED)

add_executable(qt_simple_project main.cpp)
target_link_libraries(qt_simple_project
        Qt5::Core
        Qt5::Gui
        Qt5::Widgets
)

