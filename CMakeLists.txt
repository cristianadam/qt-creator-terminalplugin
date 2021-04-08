cmake_minimum_required(VERSION 3.15)

project(TerminalPlugin)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

find_package(QtCreator COMPONENTS Core TextEditor REQUIRED)
find_package(Qt5 COMPONENTS Widgets REQUIRED)
find_package(qtermwidget5 REQUIRED)

add_qtc_plugin(TerminalPlugin
  PLUGIN_DEPENDS
    QtCreator::Core QtCreator::TextEditor
  DEPENDS Qt5::Widgets qtermwidget5
  SOURCES
    terminalplugin.cpp terminalplugin.h
    terminalwindow.cpp terminalwindow.h
)
