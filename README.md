# SYNOPSIS
A small debugging library inspired by [this][0].

# MOTIVATION
I was trying to log  something in C++ and remembered two things... 1. the
only way to log  anything in C++ is with a huge obnoxious framework and 2.
seriously, GTFO.

# USAGE
This module is designed to work with the [`datcxx`][0] build tool. To add this
module to your project us the following command...

```bash
build add heapwolf/debug
```

If the `DEBUG` environment variable is contained in the `name` that the instance
is contstructed with, the debug output be printed. For example...


#### COMMAND
```bash
DEBUG=bands ./musicprogram
```

#### CODE
```c++
#include "./deps/heapwolf/debug/index.hxx"

Debug d("bands");

//
// The instance can then be called with any number of arbitrary types.
//
d("danzig", 100, 'x');
```

#### OUTPUT

```
bands danzig 100 x
```

# TEST

```bash
build test
```


# API

## CONSTRUCTOR

### Debug d(const std::string& name[, std::ostream& stream])
Construct with a name, optionally specify an output stream.

[0]:https://github.com/visionmedia/debug
