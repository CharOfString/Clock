cmake_minimum_required(VERSION 3.28)
project(charclock)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

find_package(Qt6 COMPONENTS
        Core
        Gui
        Widgets
        REQUIRED)

add_executable(charclock
        res/resources.qrc
        src/main.cxx
        src/mainwindow/mainwindow.cxx
        src/mainwindow/mainwindow.hxx
)

target_link_libraries(charclock
        Qt::Core
        Qt::Gui
        Qt::Widgets
)
