cmake_minimum_required(VERSION 3.0.0)
project(test_nlopt VERSION 0.1.0)

# windows下git和cmake有冲突，需要加这一句话
set(CMAKE_MAKE_PROGRAM NOTFOUND)    

find_package(Nlopt)

add_executable(test_nlopt main.cpp)

target_link_libraries(test_nlopt ${NLOPT_LIBRARIES})
