# osc-motion-control

## Dev setup

### macOS
- After cloning: `git submodule update --init --recursive` to bring in external dependencies
- Toolchains etc.
    - `brew install cmake`
    - `brew tap ArmMbed/homebrew-formulae`
    - `brew install arm-none-eabi-gcc`
- VS Code
    - Install the CMake Tools extension
    - When prompted for a compiler, choose `GCC for arm-none-eabi`
- Makefile generation via `cmake`
    - `cmake . -DPICO_BOARD=pico_w -DWIFI_SSID="YourNetworkSSID" -DWIFI_PASSWORD="YourWifiPassword"`
- Building any particular particular project
    - `cd firmware/osc-stepper-controller`
    - `make`
    - Then copy the built `.uf2` to the PicoW after attaching the PicoW to USB while holding the boot loader button

## References

- [Getting started with Pico in C++](https://datasheets.raspberrypi.com/pico/getting-started-with-pico.pdf)
- [Pico SDK documentation](https://www.raspberrypi.com/documentation/pico-sdk/index_doxygen.html)

