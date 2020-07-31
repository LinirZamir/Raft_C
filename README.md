# Raft_C
This is a library which implements [Raft Consensus Algorithm](https://raft.github.io/), which is used to achieve an agreement for the state of the server as the state changes. 

## Usage

The `Raft::Server` class represents one server in the cluster. It holds the persistance and volatile server state that is specific to the algorithm.
The actual "log", as described by the algorithm, is handled as an abstraction so that the algorithm can be applied to many different server implementations. 

## Supported platforms / recommended toolchains

This is a C application which depends on the C compiler and standard C library. The program currently compiles for Linux, and it supported on almost any platform.  The following are recommended toolchains for popular platforms. 

* Windows -- [Visual Studio](https://www.visualstudio.com/) (Microsoft Visual C++)
* Linux -- clan or gcc
* MacOS -- Xcode (clang)

## Building

This library is not intended to stand alone. It is intended to be included in a larger project which uses Makefile or [CMake](https://cmake.org/) to generate the build system and build applications which will link with the library. 

There are two distinct steps in the build process: 

1. Generation of the build system, using Makefile
2. Compiling, linking, etc.
