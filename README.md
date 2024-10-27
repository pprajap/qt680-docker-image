# Qt 6.8.0 Docker Image for Ubuntu 24.04

This repository provides Dockerfiles to build Docker images for Ubuntu 24.04 with Qt 6.8.0. The images support both `linux_gcc_64` and WebAssembly (`wasm_multithread` and `wasm_singlethread`) using Emscripten SDK (emsdk) v3.1.56.

## Introduction

This project aims to simplify the setup and usage of Qt 6.8.0 on Ubuntu 24.04 for both native Linux development and WebAssembly (Wasm) development. The provided Dockerfiles create images that include all necessary dependencies and environment configurations for building and running Qt applications.

## Features

- **Ubuntu 24.04**: The base image is Ubuntu 24.04.
- **Qt 6.8.0**: Installed for both `linux_gcc_64` and WebAssembly targets.
- **Emscripten SDK v3.1.56**: Included for WebAssembly development.
- **Environment Variables**: Pre-configured for Qt and Emscripten.

## Docker Images

### Qt 6.8.0 for Linux (gcc_64)

The `qt680-gcc64-Dockerfile` sets up an environment for building and running Qt applications on Linux using the GCC compiler.

### Qt 6.8.0 for WebAssembly (wasm_multithread and wasm_singlethread)

The `qt680-wasm-multithread-emsdk-Dockerfile` & `qt680-wasm-singlethread-emsdk-Dockerfile` sets up an environment for building and running Qt applications for WebAssembly using Emscripten SDK.

## Usage

### Building the Docker Images

To build the Docker images, use the following commands:

#### Qt 6.8.0 for Linux (gcc_64)

```sh
docker build -t qt680-gcc64 -f qt680-gcc64-Dockerfile .
docker build -t qt680-wasm-multithread-emsdk -f qt680-wasm-multithread-emsdk-Dockerfile .
docker build -t qt680-wasm-singlethread-emsdk -f qt680-wasm-singlethread-emsdk-Dockerfile .