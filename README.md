`libuvc` is a cross-platform library for USB video devices, built atop `libusb`.
It enables fine-grained control over USB video devices exporting the standard USB Video Class
(UVC) interface, enabling developers to write drivers for previously unsupported devices,
or just access UVC devices in a generic fashion.

## Getting and Building libuvc

Prerequisites: You will need `libusb` and [CMake](http://www.cmake.org/) installed.

To build, you can just run these shell commands:

    git clone https://github.com/ktossell/libuvc
    cd libuvc
    mkdir build
    cd build
    cmake ..
    make && sudo make install

Instructions from https://int80k.com/libuvc/doc/ read instead:

	git clone https://github.com/ktossell/libuvc.git
	cd libuvc
	mkdir build
	cd build
	cmake -DCMAKE_BUILD_TYPE=Release ..
	make && make install

In the final analysis, we used the following line, on Windows Linux, to make the configuration
	cmake -DCMAKE_BUILD_TYPE=Release -DLIBUSB_INCLUDE_DIRS=/usr/include/libusb-1.0 ..

and you're set! If you want to change the build configuration, you can edit `CMakeCache.txt`
in the build directory, or use a CMake GUI to make the desired changes.

## Developing with libuvc

The documentation for `libuvc` can currently be found at https://int80k.com/libuvc/doc/.

Happy hacking!
