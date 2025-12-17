# From official documentation for pkgconfig
find_package(PkgConfig)
pkg_search_module(GTEST REQUIRED gtest_main)

add_executable(multiply_test multiply_test.cpp)

target_link_libraries(multiply_test
  PRIVATE
  multiply
  ${GTEST_LDFLAGS}
)
target_compile_options(multiply_test
  PRIVATE
  ${GTEST_CDFLAGS}
)

add_test(multiply_gtests multiply_test)
