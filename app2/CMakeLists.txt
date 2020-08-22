add_executable(app2 main.cpp)

OPTION(BUILD_PACK2 "Used to build package2" OFF)

include(${CMAKE_SOURCE_DIR}/cmake/CMakeLists.txt)

if (BUILD_PACK2)
    install(TARGETS app2 DESTINATION app2)
    set(CPACK_COMPONENTS_ALL app2)
    set(CPACK_PACKAGE_FILE_NAME "App2")
    create_cpack_config(CPackConfig-App2.cmake)
endif()


