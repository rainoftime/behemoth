# No debugging and optimization for examples
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O2 -DNDEBUG")

function(add_example name)
  add_executable(${name} ${name}.cpp)
  target_link_libraries(${name} behemoth behemoth_cli11)
endfunction()

add_example(demo demo.cpp)
add_example(ltl ltl.cpp)
add_example(ctl ctl.cpp)
