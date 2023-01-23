project(libjansson2)
cmake_minimum_required(VERSION 3.20)

add_library(libjansson2)
target_compile_options(libjansson2 PRIVATE -Wall -Wextra)
set_target_properties(libjansson2 PROPERTIES C_STANDARD 11)

target_include_directories(libjansson2 PUBLIC include)
add_subdirectory(src)

file(CONFIGURE OUTPUT .gitignore
  NEWLINE_STYLE UNIX
  CONTENT "*")
