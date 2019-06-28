cmake_minimum_required(VERSION 2.8.12)
project(tetgen)

add_executable(tetgen tetgen.cxx predicates.cxx)
target_compile_definitions(tetgen PRIVATE )
if(WIN32)
   target_compile_definitions(tetgen PRIVATE  )
endif()

# Generate position independent code
set_target_properties(tetgen PROPERTIES POSITION_INDEPENDENT_CODE ON)
