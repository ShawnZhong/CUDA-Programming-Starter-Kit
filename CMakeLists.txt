cmake_minimum_required(VERSION 3.16)
project(CUDA_Progrsamming_Starter_Kit)

set(CUDA_INCLUDE_DIR "${PROJECT_SOURCE_DIR}/include/CUDA-10.2")
set(LIBCXX_INCLUDE_DOR "${CUDA_INCLUDE_DIR}/cuda/std/detail/libcxx/include" )
set(LIBC_INCLUDE_DOR "${PROJECT_SOURCE_DIR}/include/musl-libc-1.1.24" )

add_definitions(-include ${LIBCXX_INCLUDE_DOR}/cstdlib)
add_definitions(-include ${CUDA_INCLUDE_DIR}/cuda_runtime_api.h)
add_definitions(-include ${CUDA_INCLUDE_DIR}/device_launch_parameters.h)
add_definitions(-include ${CUDA_INCLUDE_DIR}/device_functions.h)

include_directories(SYSTEM ${LIBC_INCLUDE_DOR})
include_directories(SYSTEM ${LIBCXX_INCLUDE_DOR})
include_directories(SYSTEM ${CUDA_INCLUDE_DIR})

add_compile_definitions(__CUDACC__)
add_compile_definitions(__GNUC__)

add_executable(example example.cu example.cpp)
set_source_files_properties(example.cu PROPERTIES LANGUAGE CXX)
set_target_properties(example PROPERTIES LINKER_LANGUAGE CXX)