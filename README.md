# Graphical Wall Clock
Lightweight graphic wall-clock using **[OpenGL](https://www.opengl.org)** and **[FreeGLUT](http://freeglut.sourceforge.net)**. Instead of drawing each hand based on the current system time each frame, this generates an inital X, Y, ΔX, and ΔY for each hand from a single snapshot, then updates X and Y each iteration using the Runge-Kutta method. To account for clockspeed variataion, delta time is adjusted based on the average frametimes for the redisplay function.

### Linux FreeGLUT install

#### Debian based
`sudo apt-get install freeglut3-dev`

#### Arch based
`sudo pacman -S freeglut`

### Windows FreeGLUT install
Download the respective prepackaged [Windows binary](https://www.transmissionzero.co.uk/software/freeglut-devel/) for either MSVC or MinGW, then place the x86 library files at the root of the project. For use with Visual C++, the third-party lib and include folders can be linked in project properties to circumvent placing each library file in the project folder.

---

![example](clock.gif)
