# [PhantomJS](http://phantomjs.org) - Scriptable Headless WebKit

PhantomJS is free software/open source, and is distributed under the [BSD license](http://opensource.org/licenses/BSD-3-Clause). It contains third-party code, see the included `third-party.txt` file for the license information on third-party code.

## Use Cases

- **Headless web testing**. Lightning-fast testing without the browser is now possible!
- **Page automation**. [Access and manipulate](http://phantomjs.org/page-automation.html) web pages with the standard DOM API, or with usual libraries like jQuery.
- **Screen capture**. Programmatically [capture web contents](http://phantomjs.org/screen-capture.html), including CSS, SVG and Canvas. Build server-side web graphics apps, from a screenshot service to a vector chart rasterizer.
- **Network monitoring**. Automate performance analysis, track [page loading](http://phantomjs.org/network-monitoring.html) and export as standard HAR format.

## Features

- **Multiplatform**, available on major operating systems: Windows, Mac OS X, Linux, and other Unices.
- **Fast and native implementation** of web standards: DOM, CSS, JavaScript, Canvas, and SVG. No emulation!
- **Pure headless (no X11) on Linux**, ideal for continuous integration systems. Also runs on Amazon EC2, Heroku, and Iron.io.
- **Easy to install**: [Download](http://phantomjs.org/download.html), unpack, and start having fun in just 5 minutes.

## Installation

System requirements:
  * C++ toolchain such as g++ 7 or later
  * CMake version 3.5 or later
  * Qt 5 toolkit
  * Community QtWebKit version 5.212 or later
  * Python 2.7 (to run the tests)


### Unix Systems

Due to the required QtWebKit >= 5.212, only the following distributions will be supported:

  * Debian 10 (buster) or later
  * Ubuntu 18.04 (bionic) or later
  * Fedora 28 or later

Install required packages:

``` bash
  sudo apt install g++ cmake qt5-default libqt5webkit5-dev python
```

Unpack source or clone the repository:

``` bash
  ./configure && make
```

Sanity check:

``` bash
  ./bin/phantomjs --version
```

Run test suite:

``` bash
  make check
```

Install:

``` bash
  make install
```

### Windows


Only MinGW is supported for now. From "MYS2 MinGW64 32-bit" shell, install the required packages:

``` powershell
  pacman -S msys/make
  pacman -S mingw32/mingw-w64-i686-toolchain
  pacman -S mingw32/mingw-w64-i686-cmake
  pacman -S mingw32/mingw-w64-i686-qtwebkit
  pacman -S mingw32/mingw-w64-i686-python2
```

Note: add --disable-download-timeout as an additional argument, if the installation failed due to the slow server responses.

After unpacking the source tarball or cloning the repository:

``` powershell
  cmake . -G "MinGW Makefiles"
```

And then start the build process:

``` powershell
  make
```

Do a quick sanity check:

``` powershell
  ./bin/phantomjs.exe --version
```

### macOS

TBD

## Questions?

- Explore the complete [documentation](http://phantomjs.org/documentation/).
- Read tons of [user articles](http://phantomjs.org/buzz.html) on using PhantomJS.
- Join the [mailing-list](http://groups.google.com/group/phantomjs) and discuss with other PhantomJS fans.

