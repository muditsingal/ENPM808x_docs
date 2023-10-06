# ENPM808x_docs

## Basic tools to install
```
sudo apt update
sudo apt install build-essential cmake ccache bear clangd
sudo apt install doxygen
sudo apt install cppcheck
pip install cpplint
```

### C++ project building
```
cmake -S ./ -B build/
cmake --build build/
```

### How to apply google formatting to written codes in C++
`clang-format -i --style=Google app/main.cpp`

`clang-format -i --style=Google $(find . -name *.cpp -o -name *.hpp | grep -vE -e "^./build/")`

### Running cppcheck
* If you need to install cppcheck, do
`sudo apt install cppcheck`

* Run in the top-level project directory (eg., in cpp-boilerplate-v2/)
`cppcheck --enable=all --std=c++11 -I include/ --suppress=missingInclude $( find . -name *.cpp | grep -vE -e "^./build/" )`


### Running clang-format
* first install clangd-format, if needed
`sudo apt install clangd-format`

* Now, you can see the reformatted output
`clang-format -style=Google your_file.cpp`

* If you want to completely replace the source code (ie., keep changes in-place) do:
`clang-format -style=Google -i your_file.cpp`


### Running cpplint
* You may need to install cpplint
`sudo apt install cpplint`

* run in the top-level project directory (eg., in cpp-boilerplate-v2/)
`cpplint --filter="-legal/copyright" $( find . -name *.cpp | grep -vE -e "^./build/" )`


