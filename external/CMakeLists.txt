include(FetchContent)

# pybind11
FetchContent_Declare(
  pybind11
  GIT_REPOSITORY https://github.com/pybind/pybind11
  GIT_TAG a2e59f0e7065404b44dfe92a28aca47ba1378dc4 # 2.10.4
)

FetchContent_MakeAvailable(pybind11)

# libsamplerate
set(BUILD_TESTING OFF CACHE BOOL "Disable libsamplerate test build")

FetchContent_Declare(
  libsamplerate
  GIT_REPOSITORY https://github.com/coder-free/libsamplerate
  GIT_TAG 4947cde5e5710b0d14c52e4dc58a9a76bc51770a # 0.2.2
)
set(LIBSAMPLERATE_VERSION 0.2.2 CACHE STRING PUBLIC)  # <-- update libsamplerate version here

FetchContent_MakeAvailable(libsamplerate)
