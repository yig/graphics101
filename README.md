Computer Graphics - Homework Assignments
========================================

These programming projects accompany an introductory computer graphics course.
They cover 2D raster images, 3D geometry, 3D transformations, ray tracing, and the GPU-accelerated graphics pipeline. The assignments have been tested on Mac, Windows, and Linux.

The courses assume familiarity with basic linear algebra, multivariable calculus, and low-level or systems programming.

Homework Assignments:
---------------------

1. [Airbrush](https://github.com/yig/graphics101-airbrush): Raster images and compositing.
2. [Raycasting](https://github.com/yig/graphics101-raycasting): Ray tracing and 3D transformations.
3. [Raytracing](https://github.com/yig/graphics101-raytracing): Ray tracing and illumination.
4. [Image Processing](https://github.com/yig/graphics101-imageprocessing): Image processing.
5. [Meshes](https://github.com/yig/graphics101-meshes): Mesh processing.
6. [Shaders aka the Graphics Pipeline](https://github.com/yig/graphics101-pipeline): The graphics pipeline and GPU shader programming.

Getting Started
---------------

* All assignments will be written in C++. The assignments should ease you in.

* You will need a working C++ compiler, the [CMake](https://cmake.org/) build system, and, for the first assignment only ([Airbrush](https://github.com/yig/graphics101-airbrush)), the [Qt GUI library](https://www.qt.io/download-open-source). Qt also has a nice integrated development environment (IDE) for C++ called Qt Creator, which is quite useful. Here are my recommended installation instructions:

    * Ubuntu Linux: `apt-get install build-essential cmake qtbase5-dev qtcreator`

    * Mac:
    
        1. Install the [Xcode](https://itunes.apple.com/us/app/xcode/id497799835) compiler and IDE.
        2. Install the [Homebrew](https://brew.sh/) package manager.
        3. On the command line, run: `brew install cmake qt` and, if you want the Qt IDE, `brew cask install qt-creator`.
        * You can use the [Qt offline installers](https://www.qt.io/offline-installers) (no account needed) or the [Qt online installer](https://www.qt.io/download-open-source) instead of steps 2 and 3. Install only the latest version of Qt and, optionally, the Qt Creator IDE.

    * Windows: There is a simpler way and a more complicated way:

        * Simpler: Use [Qt's online installer](https://www.qt.io/download-open-source). Install the open source version of the Qt environment. This annoyingly requires you to create an account, but in exchange provides a single installer for Qt Creator, the Qt library, and a C++ compiler. The online installer, by default, includes all versions of Qt. This is unnecessary and takes a huge amount of space. Install only the most recent version (e.g. Qt 5.15), the Qt Creator IDE, and the MingW compiler.
        
        * Less simple: Install [Anaconda](https://www.anaconda.com/products/individual) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html). (Miniconda is faster to install.) Choose the 64-bit Python 3.x version. Launch the Anaconda shell from the Start menu and run: `conda install -c conda-forge cmake git qt cxx-compiler`. If you want the Qt Creator IDE, install it via the Qt Creator button on the [Qt offline installer](https://www.qt.io/offline-installers) page.
        
        * More complicated:
        
            1. Install a compiler. It could be [Visual Studio](https://visualstudio.microsoft.com/) (not VSCode), which provides an entire IDE. It could be [MinGW](https://wiki.qt.io/MinGW).
            2. Install [CMake](https://cmake.org/).
            3. Install the Qt GUI libraries and, optionally, the Qt Creator IDE using the [Qt offline installers](https://www.qt.io/offline-installers) (no account needed) or the [Qt online installer](https://www.qt.io/download-open-source). Install only the latest version of Qt and the Qt Creator IDE.

* Download each assignment. Inside each folder there is a
file named `CMakeLists.txt`.

    * You can open it directly with the Qt Creator development
environment (IDE) if you are using that.

    * If you aren't using the Qt Creator IDE, from inside each folder, run:
    
            mkdir build
            cd build
            cmake ..
        
        Then, to compile the program, just type `make` or `cmake --build .`. There are some useful flags you can pass to `cmake`. Try:
        
        * `cmake -DCMAKE_BUILD_TYPE=Debug ..` to specify compilation with debug information for use with a debugger.
        * `cmake -DCMAKE_BUILD_TYPE=Release ..` to specify compilation of an optimized build. Your code will run much faster.
        * `cmake -DCMAKE_BUILD_TYPE=RelWithDebInfo ..` to specify compilation of an optimized build with debug information. Your code will run much faster, but you will still sort of be able to debug it (compilers move code around when optimizing).
        * `cmake -G Xcode ..` will generate a project for the Xcode IDE on macOS.
        * `cmake -G "Visual Studio 16 2019" ..` will generate a project for the Visual Studio IDE on Windows.

* Build and run the code. Make your changes. Write a `Notes.txt`. Run `cpack` to generate a `.zip` file. Hand in the `.zip` file.
