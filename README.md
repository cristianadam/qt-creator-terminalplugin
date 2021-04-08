This projects provides a terminal window in Qt Creator. The terminal library is provided by the [qtermwidget](https://github.com/cristianadam/qtermwidget) project.

![qtcreator-terminal](https://user-images.githubusercontent.com/1257414/114011012-0a7cc500-9865-11eb-9c87-3dfe0e991b26.png)

# Compilation

To compile the TerminalPlugin you need to specify in the `CMAKE_PREFIX_PATH` CMake variable the paths to:

1. Qt
1. QtCreator
1. qtermwidget

```
cmake -GNinja -S . -B build -DCMAKE_BUILD_TYPE=Release \
    "-DCMAKE_PREFIX_PATH=$USER/Qt/5.15.2/gcc_64;$USER/Projects/qtermwidget/install;$USER/Projects/QtCreator/build/install/qt-creator"

cmake --build build
```
