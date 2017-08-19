# OpenGL Kit for Windows

The following steps will guide you on how to build your **OpenGL** programs in **Windows**<sup>1</sup> with the **MinGW C++ compiler**.
You won't need an major IDE like Visual Studio or so, you can code your program directly into the cpp files. 
To compile your code to an .exe program, follow these steps:

1. Be sure you have MinGW C++ compiler installed on your Windows - https://sourceforge.net/projects/mingw/files/
2. Be sure you have recent OpenGL Libraries by upgrading the video drivers (Nvidia, AMD, or Intel)
3. Paste your source file(s) in the Kit folder. There are header and library files there as well.
4. Call a command window and run the compiler command:
```
g++ -o OpenGL.exe Source.cpp glfw3dll.a libglew32.dll.a -I include -L./ -lglew32 -lglfw3 -lopengl32
```
5. Now you can run the compiled program OpenGL.exe.

***

## Other Information:

You can change parameters in the compiler command:
- Change **OpenGL.exe** parameter to rename your compiled program
- Change **Source.cpp** parameter to use a different source file
- Change the **"-I include"** parameter to adapt your need to include files

On the example file provided, **"Source.cpp"**, two libraries are being used: 
- GLFW, that starts the OpenGL "context".
- GLEW, that runs the latest version of GL and handles GL extensions.

Description for the existing files in the folder:
- Include headers in the GL and GLFW folders inside "include" folder
- Compiled library files glfw3dll.a and libglew32.dll.a
- GLFW and GLEW library files glfw3.dll and glew32.dll

This guide was based in Anton's OpenGL 4 tutorials available at:
http://antongerdelan.net/opengl/hellotriangle.html

You can find the library files along with OpenGL usage in different OS and many demos at Anton's Github page:
https://github.com/capnramses/antons_opengl_tutorials_book

If you want to contact me, please send me an e-mail - isaque.ha@gmail.com


<sup>1</sup>
This was tested in Windows 10 64 bits
