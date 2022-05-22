# protobuf-sandbox
A sandbox for playing around with various ideas related to protobuf

This project depends on the (`protobuf`)[https://developers.google.com/protocol-buffers] library.
Instructions for installation can be found (here)[https://github.com/protocolbuffers/protobuf].
You'll also need the `protobuf` python package.

## Generating protos

### Python

In order to (re)generate the python bindings for the protos:

```
cd python
protoc -I=../protos --python_out=. ../protos/*.proto
```

This will generate all of the python protos into the `python` directory.

### C++

In order to (re)generate the C++ bindings for the protos:

```
mkdir -p build
protoc -I=protos --cpp_out=build protos/*.proto
```
