set(Boost_USE_STATIC_LIBS        ON)
find_package(Boost 1.67.0 COMPONENTS filesystem program_options)
include_directories(${Boost_INCLUDE_DIRS})

add_executable(${PROJECT_NAME} main.cpp)
target_compile_features(${PROJECT_NAME} PRIVATE cxx_auto_type cxx_decltype_auto)
target_link_libraries(${PROJECT_NAME} ${Boost_LIBRARIES})

