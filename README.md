# C++ project with GLFW, IMGUI and power saving enabled

This project contains the a basic Visual Studio project 
with the following items installed:
- GLFW - https://www.glfw.org/
- ImGUI (docking branch) - https://github.com/ocornut/imgui/tree/docking
- Power saving setup for ImGUI in GLFW - https://github.com/ocornut/imgui/pull/2749

## Installation and use

1. Clone the repository:
```sh
git clone git@github.com:ionutvmi/glfw-imgui-power-saving.git
```

2. Download the pre-compiled binaries for GLFW
https://www.glfw.org/download.html

For 64bit builds:  
From the archive place the `lib-vc2019/*.dll` and `lib-vc2019/*.lib` files in the
`libs/bin-x64` folder of the `GuiApplication` project.

For 32bit builds:  
From the archive place the `lib-vc2019/*.dll` and `lib-vc2019/*.lib` files in the
`libs/bin-x86` folder of the `GuiApplication` project.

3. Open the `.sln` file with Visual Studio and press F5 to compile and run the application.


## Power saving mode

The power saving mode is enabled by default in main.cpp:

```cpp
io.ConfigFlags |= ImGuiConfigFlags_EnablePowerSavingMode;
```

To set a minimum refresh time for the UI use the `SetMaxWaitBeforeNextFrame` function.

```cpp
// this should be called AFTER `ImGui::NewFrame()` 
ImGui::SetMaxWaitBeforeNextFrame(1); // in seconds
```


## Author

Mihai Ionut Vilcu

-   [github/ionutvmi](https://github.com/ionutvmi)
-   [twitter/mihaivlc93](http://twitter.com/mihaivlc93)



