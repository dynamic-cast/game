## Installation 

### Linux

If you're using some Debian derived system, simply:

```
sudo apt install libsfml-dev
```

To download the main package, with this you have access to all 5 modules that compose SFML: system, window, graphics, network and audio.

If you don't have a look at [here](https://www.sfml-dev.org/tutorials/2.5/start-linux.php).

## Building and compiling a project

You can either use CMAKE or type a thousand flags in the command line.

### Using CMAKE

First, make sure you have all of these dependencies:

* freetype
* x11
* xrandr
* udev
* opengl
* flac
* ogg
* vorbis
* vorbisenc
* vorbisfile
* openal
* pthread

#### On apt

```
sudo apt install cmake
```

### Typing a thousand flags

Compile it:
```
g++ -c <all_of_implementation_files.cpp>
```

Link it:
```
g++ <all_your_compiled_files.o> -o sfml-app -lsfml-graphics -lsfml-window -lsfml-system -lsfml-audio -lsfml-main
```

Execute it:
```
./sfml-app
```