cmake_minimum_required(VERSION 3.8)

if(PICO_SDK_PATH)
  include(${32BLIT_DIR}/32blit-pico/pico_sdk_import.cmake)
  include(${32BLIT_DIR}/32blit-pico/pico_extras_import.cmake)
endif()

project (blitboing)
find_package (32BLIT CONFIG REQUIRED PATHS ../32blit-sdk)
blit_executable (blitboing blitboing.cpp blitboing.hpp)
blit_assets_yaml (blitboing assets.yml)
blit_metadata (blitboing metadata.yml)