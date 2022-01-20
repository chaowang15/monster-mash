# Environment Setup and Code Usage of Monster Mash code

This repo is the Monster Mash code (https://github.com/google/monster-mash/) but with some small modifications to fix building errors on Ubuntu 18.


## Possible Errors 

Error about `filesystem`:
- https://stackoverflow.com/questions/55474690/stdfilesystem-has-not-been-declared-after-including-experimental-filesystem
- https://stackoverflow.com/questions/39231363/fatal-error-filesystem-no-such-file-or-directory


## Build code

Follow the official README in the original code. Besides the original steps: 
- Install SDL2 by:
```
sudo apt-get install libsdl2-dev
```

- Build desktop demo:
```
cmake -DCMAKE_BUILD_TYPE=Release ../../src
make -j4
```

## Code usage

Keyboard control is set up inside function `keyPressEvent()` in code `src/mainwindow.cpp`.

Common Keyboard usage:
```
Left Mouse: drag control points
Right Mouse: translation
Middle Mouse: rotation
1: original outline mode
2: 3D mesh mode
3: Animation mode. You can add control points by mouse first. Drag control points to generate animation.
e: Recording trajectory and animation too. Please it again to stop recording.
Space: pause aimation
s: Save all things into a zip file. Default: `/tmp/mm_project.zip`
l (lowercase L): load project zip file. 
n: reset entire scene.
```
