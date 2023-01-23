project(jansson2)
cmake_minimum_required(VERSION 3.20)

add_library(jansson2)
target_compile_options(jansson2 PRIVATE -Wall -Wextra)
set_target_properties(jansson2 PROPERTIES C_STANDARD 11)

target_include_directories(jansson2 PUBLIC include)
add_subdirectory(src)

file(CONFIGURE OUTPUT .gitignore
  NEWLINE_STYLE UNIX
  CONTENT "*")
