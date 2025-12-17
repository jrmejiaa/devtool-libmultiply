add_library(multiply multiply.cpp)

target_include_directories(multiply PUBLIC include)

install(TARGETS multiply PUBLIC_HEADER DESTINATION "include")
