# rendergraph-parser

Render graph configuration file parser to make programming with low-level graphics APIs fun & easy.

[![Build Status](https://app.travis-ci.com/jimbi-o/rendergraph-parser.svg?branch=main)](https://app.travis-ci.com/jimbi-o/rendergraph-parser)
[![Build status](https://ci.appveyor.com/api/projects/status/ngh5gtlhknig977l?svg=true)](https://ci.appveyor.com/project/jimbi-o/rendergraph-parser)
[![codecov](https://codecov.io/gh/jimbi-o/rendergraph-parser/branch/main/graph/badge.svg?token=JO6HS1T7C6)](https://codecov.io/gh/jimbi-o/rendergraph-parser)
[![Coverity Scan Build Status](https://scan.coverity.com/projects/24132/badge.svg)](https://scan.coverity.com/projects/jimbi-o-rendergraph-parser)

## make & build (&run) locally examples

### UNIX like

```
rm -rf build/testgcc9 && cmake -S . -B build/testgcc9 -G Ninja -DCMAKE_C_COMPILER=g++-9 -DCMAKE_CXX_COMPILER=g++-9 -DCMAKE_EXPORT_COMPILE_COMMANDS=ON -DCMAKE_CXX_COMPILER_LAUNCHER=ccache -DCPM_SOURCE_CACHE=~/dev/.cache/CPM -DBUILD_WITH_TEST=ON && cmake --build build/testgcc9 && ./build/testgcc9/rendergraphparser
rm -rf build/testclang11 && cmake -S . -B build/testclang11 -G Ninja -DCMAKE_C_COMPILER=clang-11 -DCMAKE_CXX_COMPILER=clang++-11 -DCMAKE_EXPORT_COMPILE_COMMANDS=ON -DCMAKE_CXX_COMPILER_LAUNCHER=ccache -DCPM_SOURCE_CACHE=~/dev/.cache/CPM -DBUILD_WITH_TEST=ON -DCMAKE_CXX_FLAGS="-ftime-trace" && cmake --build build/testclang11 && ./build/testgclang11/rendergraphparser
```

### Windows

```
cmake -S . -B build/testvs -DBUILD_WITH_TEST=ON && cmake --build build/testvs
build\testvs\Debug\rendergraphparser.exe
```
