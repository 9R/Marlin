# Marlin repo for x350

## Usage

### Setup venv & install platformio

> virtualenv venv
> source venv/bin/activate
> pip install platformio

## Building the firmware
> platformio run -e megaatmega2560

## Flashing the firmware

> platformio run --target upload -e megaatmega2560

or

> avrdude -c stk500v2 -P /dev/ttyUSB0 -p atmega2560   -U flash:w:.pio/build/megaatmega2560/firmware.hex:i

Warning: Currently the config does not build a working firmware
