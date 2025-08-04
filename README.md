# Flickering Screen

Old-TV static in about 40 lines of C. A window full of random pixels that changes every few milliseconds.

I built it to try SDL2 and drawing straight into the window's pixel memory.

<p align="center">
  <img src="img/tv.jpg" width="600"/>
</p>

## How it works

1. Open a 900×700 window and get its surface, the block of memory SDL shows on screen.
2. In a loop, write a random number (`rand()`) into every pixel. A random 32-bit number is a random color.
3. Tell SDL to show the surface, wait 5 ms, and repeat until the window is closed.

No shapes and no textures: just one random value per pixel, every frame.

## Requirements

- **GCC** and **SDL2** on Linux. On Windows, use WSL with Ubuntu.

## Run

In Ubuntu (or WSL), from the project folder:

```bash
sudo apt install libsdl2-dev
gcc tv.c -o tv -lSDL2
./tv
```

Close the window to quit.
