# Automatic Music Morphing

### Version 0.0.1
### This is a Python command line application.

## This is adapted from Python Image Morpher (PIM) by David Dowd. https://github.com/ddowd97/Morphing
It was one attempt to use a image morphing aproach to generate transitions between two MIDI files. Sadly the results were not satisfying.

## Current features
- No GUI, single file command line program
- batch processing: transition between many MIDIS, not just 2

## Warning
Be careful when using the required ```-outprefix``` parameter.  The program overwrites ```<outprefix><sequencenumber>.mid``` files without warning. Example: ```... -outprefix f ...``` can overwrite ```f1.mid```, ```f2.mid``` ... Backup your MIDI files before running the program and avoid name conflicts.

## Examples
Help:

```python automusicmorph.py -h```

----
This will create and save ```f1.mid```, ```f2.mid```, ... ```f4.mid```. The keyframes ```f0.mid``` and ```f5.mid``` will not be modified (overwritten), but only if the framerate matches their filename.

```python autoimagemorph.py -inframes "['f0.png','f5.png']" -outprefix f -framerate 5```

----

## Install dependencies:
```pip install scipy numpy matplotlib opencv-python miditoolkit```

## TODO:
- testing, error checks, sanity checks
- speed optimization in interpolatePoints()
- LinAlgError sometimes? Image dimensions should be even numbers?

## License
### The Unlicense / PUBLIC DOMAIN

This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to [http://unlicense.org](http://unlicense.org)
