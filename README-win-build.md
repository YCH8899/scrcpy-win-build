
# make(build) dependencies
Install MSYS2 and start its MINGW64 terminal.
Android Studio's SDK installed(by default) to sdk.dir=C\:\Users\USER\AppData\Local\Android\Sdk
JDK installed to a folder e.g. C:\Java\jdk-21

Dependencies package to be installed on MSYS2 MINGW64:
pacman -S mingw-w64-x86_64-SDL2 \
          mingw-w64-x86_64-ffmpeg \
          mingw-w64-x86_64-libusb

# client build dependencies
pacman -S mingw-w64-x86_64-make \
          mingw-w64-x86_64-gcc \
          mingw-w64-x86_64-pkg-config \
          mingw-w64-x86_64-meson

pacman -S unzip

# run the below command for building scrcpy (v2.3.1) on MSYS2 MINGW64 terminal in Windows(11) host:
$ export PATH="/c/Java/jdk-21/bin:$PATH"
$ make -f release-W64.mk

Find build results at scrcpy-win-build\dist\
