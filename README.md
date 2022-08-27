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

* You will need a working C++ compiler and the [CMake](https://cmake.org/) build system. Here are my recommended installation instructions:

    * Ubuntu Linux: `apt-get install build-essential cmake`

    * Mac:
    
        1. Install the [Xcode](https://itunes.apple.com/us/app/xcode/id497799835) compiler and IDE.
        2. Install the [Homebrew](https://brew.sh/) package manager.
        3. On the command line, run: `brew install cmake`.

    * Windows: There are two ways that should work well:

        * [Miniconda](https://docs.conda.io/en/latest/miniconda.html): Choose the 64-bit Python 3.x version. Launch the Anaconda shell from the Start menu and run: `conda install -c conda-forge cmake git cxx-compiler`.
        
        * DIY:
        
            1. Install a compiler. It could be [Visual Studio](https://visualstudio.microsoft.com/), which provides an entire IDE. It could be [MinGW](https://wiki.qt.io/MinGW). ([Visual Studio *Code*](https://code.visualstudio.com/) is a nice editor, but doesn't come with a compiler.)
            2. Install [CMake](https://cmake.org/).

* Download each assignment. Inside each folder there is a
file named `CMakeLists.txt`.

    * You can open it directly with your IDE, if your IDE supports that. (Examples: [Visual Studio](https://visualstudio.microsoft.com/vs/), [Visual Studio Code](https://code.visualstudio.com/) with the [CMake Tools extension](https://devblogs.microsoft.com/cppblog/cmake-tools-extension-for-visual-studio-code/), [CLion](https://www.jetbrains.com/clion/), and Qt Creator.)

    * You can ask `cmake` to generate a build file for your IDE. For example:
    
        * `cmake -G Xcode ..` will generate a project for the Xcode IDE on macOS.
        * `cmake -G "Visual Studio 16 2019" ..` will generate a project for the Visual Studio 2019 IDE on Windows.

    * If you aren't using an IDE, from inside each folder, run:
    
            mkdir build
            cd build
            cmake ..
        
        Then, to compile the program, just type `make` or `cmake --build .`. There are some useful flags you can pass to `cmake`. Try:
        
        * `cmake -DCMAKE_BUILD_TYPE=Debug ..` to specify compilation with debug information for use with a debugger.
        * `cmake -DCMAKE_BUILD_TYPE=Release ..` to specify compilation of an optimized build. Your code will run much faster.
        * `cmake -DCMAKE_BUILD_TYPE=RelWithDebInfo ..` to specify compilation of an optimized build with debug information. Your code will run much faster, but you will still sort of be able to debug it (compilers move code around when optimizing).

* Build and run the code. Make your changes. Write a `Notes.txt`. Run `cpack` (or `make zip` or `cmake --build . --target zip`) to generate a `.zip` file. Hand in the `.zip` file.
