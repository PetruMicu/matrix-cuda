cmake_minimum_required(VERSION 3.27)
project(matrix_cuda CUDA)

set(CMAKE_CUDA_STANDARD 17)

add_executable(matrix_cuda main.cu)

set_target_properties(matrix_cuda PROPERTIES
        CUDA_SEPARABLE_COMPILATION ON)

set(CMAKE_CUDA_FLAGS "${CMAKE_CUDA_FLAGS} -fopenmp")