cmake_minimum_required(VERSION 3.15)
project(lodepng LANGUAGES CXX)

add_library(lodepng lodepng.cpp)
set_target_properties(lodepng PROPERTIES WINDOWS_EXPORT_ALL_SYMBOLS ON)

include(GNUInstallDirs)
install(TARGETS lodepng
    RUNTIME DESTINATION "${CMAKE_INSTALL_BINDIR}"
    LIBRARY DESTINATION "${CMAKE_INSTALL_LIBDIR}"
    ARCHIVE DESTINATION "${CMAKE_INSTALL_LIBDIR}")
install(FILES lodepng.h DESTINATION ${CMAKE_INSTALL_INCLUDEDIR})
