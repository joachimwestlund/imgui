# imgui
Test with Dear ImGui SDL3 and cmake

### Compile on windows

Install Visual Studio 2026 community edition with c++ development installed

create a build directory

in that directory issue these commands:

```
cmake .. -G "Visual Studio 18 2026"
```

```
cmake --build . --config Release (or Debug)
```

copy SDL3.dll from directory "_deps\sdl3-build\Release" to directory bin\release\

start your program from directory "bin\release\myapp.exe"

### Compile on Linux

dependencies ubuntu 22.04+:

```
sudo apt install build-essential git make \
pkg-config cmake ninja-build gnome-desktop-testing libasound2-dev libpulse-dev \
libaudio-dev libfribidi-dev libjack-dev libsndio-dev libx11-dev libxext-dev \
libxrandr-dev libxcursor-dev libxfixes-dev libxi-dev libxss-dev libxtst-dev \
libxkbcommon-dev libdrm-dev libgbm-dev libgl1-mesa-dev libgles2-mesa-dev \
libegl1-mesa-dev libdbus-1-dev libibus-1.0-dev libudev-dev libthai-dev \
libpipewire-0.3-dev libwayland-dev libdecor-0-dev liburing-dev
```

create a build directory

```
cmake ..
```

```
cmake --build .
```

run ./bin/myapp
