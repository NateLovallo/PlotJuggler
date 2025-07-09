conan install .. -of . --build=missing -pr:b=default -s build_type=Release -s compiler.cppstd=17

cmake --preset conan-default -S .. -B . -DBUILDING_WITH_CONAN=ON -DCMAKE_INSTALL_PREFIX=install -DCMAKE_BUILD_TYPE=Release --fresh

cmake --build . --config Release --target install --parallel