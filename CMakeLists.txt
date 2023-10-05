cmake_minimum_required(VERSION 3.10)


project(iptest )


add_executable(iptest ip_filter.cpp)


set_target_properties(iptest PROPERTIES
    CXX_STANDARD 14
    CXX_STANDARD_REQUIRED ON
)





if(CMAKE_CXX_COMPILER_ID MATCHES "Clang" OR
CMAKE_CXX_COMPILER_ID STREQUAL "GNU")
target_compile_options(11.posl_cont PRIVATE
-g
-Wall
-Wextra
-Werror
-pedantic)

elseif(CMAKE_CXX_COMPILER_ID STREQUAL "MSVC")
target_compile_options(posl_cont PRIVATE
/EHsc
/W4
/WX)
endif()




