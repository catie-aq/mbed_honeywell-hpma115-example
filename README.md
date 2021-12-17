# Honeywell HPMA115 driver example app
Usage example for the Honeywell HPMA115 driver

## Requirements
### Hardware requirements
The following boards are required:
- Zest Sensor Dust
- Zest Core MTXDot

### Software requirements
Honeywell HPMA115 driver example app makes use of the following libraries (automatically
imported by `mbed deploy` or `mbed import`):
- honeywell-hpma115
- zest-core-mtxdot

## Usage
To clone **and** deploy the project in one command, use `mbed import` and skip to the
target enabling instructions:
```shell
mbed import https://gitlab.com/koncepto/CATIE/3sqair/software/honeywell-hpma115-example.git honeywell-hpma115-example
```

Alternatively:

- Clone to "honeywell-hpma115-example" and enter it:
  ```shell
  git clone https://gitlab.com/koncepto/CATIE/3sqair/software/honeywell-hpma115-example.git honeywell-hpma115-example
  cd honeywell-hpma115-example
  ```

- Deploy software requirements with:
  ```shell
  mbed deploy
  ```

Enable the custom target:
```shell
cp zest-core-mtxdot/custom_targets.json .
```

Compile the project:
```shell
mbed compile
```

Program the target device with a Segger J-Link debug probe and
[`sixtron_flash`](https://gitlab.com/catie_6tron/6tron-flash) tool:
```shell
sixtron_flash stm32l151cc BUILD/ZEST_CORE_MTXDOT/GCC_ARM/honeywell-hpma115-example.elf
```

Debug on the target device with the probe and Segger
[Ozone](https://www.segger.com/products/development-tools/ozone-j-link-debugger)
software.
