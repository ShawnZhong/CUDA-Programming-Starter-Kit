# CUDA Programming Starter Kit

CUDA programming with autocompletion, error-checking, jump-to-definition and quick documentation!

This repo provides basic functionalities for **editing** `*.cu` and `*.cuh` files without the need to install any dependencies (e.g., You don't need to install `nvcc`, `gcc`, `clang`, `msvc`, or any other toolchains). 

If you want to compile, run, and/or debug CUDA programs, please install the CUDA Toolkit from [here](https://developer.nvidia.com/cuda-toolkit).

## VSCode

### Usage

1. Install the C/C++ Plugin https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools

2. Clone this repo and open it in VSCode

### Features

- Autocomplete 

    ![image-20200215232640853](assets/image-20200215232640853.png)

- Error Checking

    ![image-20200215234448029](assets/image-20200215234448029.png)

- Quick Documentation

    ![image-20200215234654292](assets/image-20200215234654292.png)


## CLion

### Usage

1. Open the preference and register the file extension `*.cu` and `*.cuh` as C/C++ files (See screenshot below)

2. Clone this repo and open it in CLion

	![image-20200215235421482](assets/image-20200215235421482.png)

### Features

- Autocomplete 

    ![image-20200215232927428](assets/image-20200215232927428.png)

- Error Checking

    ![image-20200215233108863](assets/image-20200215233108863.png)

- Quick Documentation

    ![image-20200215234901712](assets/image-20200215234901712.png)


## Known Issues

- Do not support the `<<<`/`>>>` syntax. Everything else is supported. 

## Tests

- Tested on a fresh copy of Windows 10 (with no toolchains)

- Tested on a fresh copy of Ubuntu 19.10 (with no toolchains)

- Tested on macOS Catalina with Apple clang version 11.0.0

- Tested on Windows 10 with MinGW GCC

