cmake_minimum_required(VERSION 2.8.3)
project (sidh)
add_definitions(-D_AMD64_ -D__LINUX__) #TODO set this flags automatically
add_library(sidh ec_isogeny.c fpx.c kex.c SIDH.c SIDH_setup.c validate.c generic/fp_generic.c)

add_executable(test tests/kex_tests.c tests/test_extras.c)
target_link_libraries(test sidh)
