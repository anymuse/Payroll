project(PayrollTests)

set(CATCH_INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/lib)
add_library(Catch INTERFACE)
target_include_directories(Catch INTERFACE ${CATCH_INCLUDE_DIR})

set(TEST_SOURCES
        ${CMAKE_CURRENT_SOURCE_DIR}/main.cpp
        )
add_executable(tests ${TEST_SOURCES})
target_link_libraries(tests Catch)