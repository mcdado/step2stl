# step2stl
Example program of how to convert ISO 10303 STEP files (AP203 and AP 214) to STL using OpenCascade

## Dependencies

You need OpenCascade.

### Linux

On Ubuntu you can try to install OpenCascade from apt. This might work:

```
sudo apt install \
    liboce-foundation-dev \
    liboce-modeling-dev \
    liboce-ocaf-dev \
    liboce-ocaf-lite-dev \
    liboce-visualization-dev \
    # oce-draw # this is optional
```

### Compiling OpenCascade from source:

#### Linux

```
make
```

#### macOS

To compile from source (on macOS make sure to use gcc, not clang):

```
git clone https://github.com/tpaviot/oce.git
git checkout 13965711913c4590549de562e55c922fb0889d24
cd ..
cd oce
mkdir build
cd build
cmake ..
sudo make install
```


## Compiling

You should be able to compile it on ubuntu or osx if you have
OpenCascade installed (Makefile included). The included Makefile
assumes the library paths as used by the source installation route. If
you install from apt, then you may need to remove `local/` from some
of the paths.

## Running

Once you have compiled it,
just use it as:

```
./step2stl STEPFILENAME STLFILENAME
```

## Using in node.js

Run `make lib` to create the dynamic library and ffi file for use in node.js.

