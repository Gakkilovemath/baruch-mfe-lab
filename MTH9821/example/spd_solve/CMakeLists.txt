cmake_minimum_required(VERSION 2.6)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -Wall -Wno-long-long -Wno-deprecated -pedantic")

include_directories(./ 
                    ../../cholesky/ 
                    ../../triangular_solve/ 
                    ../../../../lib/eigen/)
 
# Link runTests with what we want to test and the GTest and pthread library
add_executable(runSpdSolve
               ./main.cpp
               ../../cholesky/cholesky.cpp
               ../../triangular_solve/triangular_solve.cpp)

