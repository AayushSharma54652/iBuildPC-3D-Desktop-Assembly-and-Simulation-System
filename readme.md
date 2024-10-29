# iBuildPC: Interactive Desktop Assembly Simulation

## Introduction  
**iBuildPC** is a graphical simulation project that allows users to interactively explore and assemble components of a desktop computer. Built with **OpenGL** and other essential graphics libraries, the project focuses on rendering 3D components of a PC and enabling user interactions to explore each part in detail.

## Features  
- **3D Interactive Visualization**: View and interact with various components like CPU, GPU, RAM, motherboard, cooling fan, etc.
- **Modular Design**: Different modules manage the core, input, text, and transformation functions.
- **User-Friendly Input**: Interact using mouse clicks and keyboard inputs to explore or transform views.
- **Transformation Module**: Switch between generic views and specific parts.
- **Text Module**: Provides detailed descriptions of selected components.

## Tech Stack  
- **Programming Language**: C / C++
- **Libraries Used**:  
  - **OpenGL**: Rendering and display.
  - **GLFW**: Window creation and input handling.
  - **GLUT**: Utilities for managing OpenGL windows.
  - **FreeType**: Handling fonts and text rendering.
  - **Vulkan API**: Potential future enhancement for rendering.

## Project Structure  
1. **Object Module**: Models CPU cabinets, motherboard, and other hardware components.
2. **Input Module**: Captures user interactions like mouse clicks or key presses.
3. **Transformation Module**: Alters views to focus on specific parts.
4. **Text Module**: Displays detailed information about selected components.
5. **Display Module**: Renders the scenes using bitmaps and textures.

## Flowchart  
The overall process flow involves:
1. User interacts with components via input devices (mouse, keyboard).
2. Input data is passed to the **Transformation Module**.
3. The system updates the view and displays text-based information using the **Text Module**.

## Implementation  
- **Bitmap Loader**: Renders text in the 3D environment.
- **Texture Map Loader**: Applies bitmap images as textures onto 3D models.
- **drawCPU Method**: Assembles and renders all components in the scene.
- **Motherboard Surface Creation**: Demonstrates texture mapping on the motherboard surface.

## Snapshot

Instance | Image
--- | ---
Initial View | <img src="https://user-images.githubusercontent.com/48080453/60199807-5a41f600-9862-11e9-849c-9f65a8638e0d.png" alt="initial view of system" style="max-height: 80px;"/>
CPU View | <img src="https://user-images.githubusercontent.com/48080453/60199855-73e33d80-9862-11e9-9d0f-3606fbb0bbb8.png" alt="cpu view" style="max-height: 80px;"/>
Desktop View | <img src="https://user-images.githubusercontent.com/48080453/60199856-73e33d80-9862-11e9-850e-467f089f63cc.png" alt="desktop" style="max-height: 80px;"/>

## Setup Project

 ### Windows
  1. Setup the project with required OpenGL headerfiles in your IDE (refer this - [Visual Studio](https://www.youtube.com/watch?v=k9LDF016_1A) or [CodeBlocks](https://www.youtube.com/watch?time_continue=79&v=Le4ub4apbn0)).
  2. Copy all required __header files & data files__ the project.
  3. Run the project. `main.cpp`
  
 > **Note**: BMP Image Error - `parameter.h` change _BMP images_ path to either **Relative** to project *( Currently )* or **Absolute**  *( if error occurs )*

 ### MacOS
 Instructions to run on MacOS
 
 Install **brew**
 ```
 /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
 ```
 
 Install necesarry linking libraries
 ```
 brew install freeglut glfw3 glew lstdc++
 ```
 
 Compile project into binary
 ```
 clang -o main main.cpp -L/usr/local/lib -lglfw -lstdc++ -framework OpenGL -framework GLUT -framework Cocoa
 ```
 
 Run the binary
 ```
 ./main
 ```

 > **Note**: GLUT is getting deprecated on MacOS 10.9 above, so some functionalities might not work. Need to fix these deprecations soon

---
  
## Controls
  - `Up Arrow` - Move Forwards
  - `Down Arrow` - Move Backwords
  - `Left Arrow` - Move Left Side
  - `Right Arrow` - Move Right Side
  - `Esc` - Exit of Program / Exit of CPU View ( according to context )
  - `Enter` - Enter into CPU View / Disassemble Components ( according to context )
  - `Backspace` - Assemble components
  - `Mouse Hover` - Change Camera View & Rotate Person
  
---

## Requirements
  - (optional) IDE ( *Visual Studio / CodeBlocks* )\*
  - basic C++ Libraries
  - glut.h ( freeglut )
    
---




## Future Enhancements  
1. Add more interactive features and component variations.
2. Allow users to benchmark their assembled PC configurations.
3. Integrate Vulkan API for improved rendering performance.

## Conclusion  
The **iBuildPC** project offers a hands-on experience in understanding computer components through interactive 3D simulations. With the help of OpenGL’s powerful rendering capabilities, it provides an intuitive way to learn about the assembly and functionality of desktop PCs.

## References
  1. Basic 3D World Setup - [lighthouse3d.com](http://www.lighthouse3d.com/tutorials/glut-tutorial/).
  2. Basic OpenGL function's introduction - [khronos.org](https://www.khronos.org/).
  3. Texture Mapping - [youtube.com](https://www.youtube.com/watch?v=Eh0HeTCCgnE&t=452s).
  4. Textbook for understanding structure of OpenGL - [Computer Graphics With OpenGL - Donald Hearn & Pauline Baker](https://doc.lagout.org/programmation/OpenGL/Computer%20Graphics%20with%20OpenGL%20%284th%20ed.%29%20%5BHearn%2C%20Baker%20%26%20Carithers%202013%5D.pdf).
  
---