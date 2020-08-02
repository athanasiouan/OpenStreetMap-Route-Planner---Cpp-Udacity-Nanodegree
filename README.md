# Route Planning Project

This project implements a A* route planner running on OpenStreetMap in C++, similar to what is used on professional router planners like Google Maps.

It can calculate and draw the shortest path from point a to point b. The user enters two coordinates with x and y between 0 and 100, then the map is drawn using the io2d library and the shortest path is rendered in orange:

<img src="map.png" width="600" height="450" />

## Dependencies for Running Locally
* cmake >= 3.11.3
  * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1 (Linux, Mac), 3.81 (Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* gcc/g++ >= 7.4.0
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same instructions as make - [install Xcode command line tools](https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)
* IO2D
  * Installation instructions for all operating systems can be found [here](https://github.com/cpp-io2d/P0267_RefImpl/blob/master/BUILDING.md)
  * This library must be built in a place where CMake `find_package` will be able to find it

## Compiling and Running

### Compiling
You need to install io2d and its dependencies first. Under Windows, you can use [vcpkg](https://github.com/microsoft/vcpkg) to do that easily:

```
vcpkg install io2d:x64-windows
```

To compile the project, first, create a `build` directory and change to that directory:

```
mkdir build && cd build
```
From within the `build` directory, then run `cmake` and `make` as follows and change the path to your vcpkg directory:
```
cmake -DCMAKE_TOOLCHAIN_FILE=vcpkg_root/scripts/buildsystems/vcpkg.cmake -DCMAKE_GENERATOR_PLATFORM=x64 ..
make
```
Now the CppND-Route-Planning-Project executable should have been created in the /bin folder.


### Running

The executables will be placed in the `bin` directory. From within `build`, you can run the project as follows:
```
../bin/CppND-Route-Planning-Project -f ../map.osm
```

## Testing

The testing executable is also placed in the `build` directory. From within `build`, you can run the unit tests as follows:
```
./test
```

