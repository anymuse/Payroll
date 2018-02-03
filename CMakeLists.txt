cmake_minimum_required(VERSION 3.9)
project(Payroll)

set(CMAKE_CXX_STANDARD 17)

set(SOURCE_FILES main.cpp)

add_executable(payroll_run ${SOURCE_FILES})


add_subdirectory(Payroll)
add_subdirectory(PayrollTests)

target_link_libraries(payroll_run Payroll)