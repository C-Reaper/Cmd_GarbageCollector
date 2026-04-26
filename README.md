# Project README

## Overview
This project is a simple implementation of a garbage collector in C. The primary focus is on managing memory allocation, deallocation, and sharing between different parts of the application.

## Features
- Memory Allocation (`GarbageCollector_Alloc`)
- Memory Deallocation (`GarbageCollector_Free`)
- Sharing Memory Between Owners (`GarbageCollector_Share`)

## Project Structure

### Prerequisites
- C/C++ Compiler (GCC, Clang)
- Make utility
- Standard development tools

## Build & Run
To build and run the project:

1. **Navigate to the project directory**:
   ```sh
   cd /home/codeleaded/Hecke/C/Cmd_GarbageCollector
   ```

2. **Build the project for Linux** (assuming `gcc` is installed):
   ```sh
   make -f Makefile.linux all
   ```

3. **Run the compiled program**:
   ```sh
   ./build/Main
   ```

4. **Build and run for Windows** (assuming `gcc` is installed on a Linux system):
   ```sh
   make -f Makefile.windows all
   ```
   Then, you may need to use Wine to run the executable:
   ```sh
   WINEPREFIX=~/wine64 WINEARCH=win64 wine build/Main.exe
   ```

5. **Build and run for Web Assembly** (assuming `clang` is installed):
   ```sh
   make -f Makefile.web all
   ```
   Then, you can use `wasmtime` to run the compiled WebAssembly file:
   ```sh
   wasmtime build/Main.wasm
   ```

6. **Clean up and rebuild**:
   ```sh
   make -f Makefile.linux clean
   make -f Makefile.linux all
   ```

7. **Build with debugging symbols**:
   ```sh
   make -f Makefile.linux alldebug
   ```
   Then, use GDB to debug the program:
   ```sh
   gdb ./build/Main
   ```