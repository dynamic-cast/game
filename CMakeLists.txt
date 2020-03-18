cmake_minimum_required(VERSION 3.6)
project(sfml-app)

find_package(SFML 2.5 COMPONENTS system window graphics audio REQUIRED)

add_executable(sfml-app src/main.cpp)

target_compile_features(sfml-app
                        PRIVATE
                        cxx_std_17)

target_compile_options(sfml-app
                       PRIVATE
                       $<$<CXX_COMPILER_ID:MSVC>:/W3 /permissive- /TP>
					   $<$<CXX_COMPILER_ID:GNU>:-Wall -Wextra>)

# Any additional include files would go here
#target_include_directories(sfml-app
#                           PUBLIC
#                           )

target_compile_definitions(sfml-app
                           PRIVATE
                           $<$<CONFIG:Debug>:DEBUG>)

target_link_libraries(sfml-app
                      PRIVATE
                      sfml-graphics)
