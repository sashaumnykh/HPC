cmake_minimum_required(VERSION 3.22)
project(HPC)

set(CMAKE_CXX_STANDARD 14)

find_package(MPI REQUIRED)
find_package(OpenMP REQUIRED)

add_executable(HPC OMP/quicksort.cpp OMP/matrix.cpp OMP/pi.cpp MPI/matrix.cpp MPI/quicksort.cpp MPI/pi.cpp)
target_link_libraries(HPC PUBLIC MPI::MPI_CXX)
