# The Frood

<img src="https://github.com/piit79/Frood/blob/main/Frood-back.png?raw=true" width="200" align="right">
<img src="https://github.com/piit79/Frood/blob/main/Frood-front.png?raw=true" width="200" align="right">

The Frood is a high-performance _and_ affordable Pro Micro drop-in replacement based on a Raspberry Pi RP2040. It is physically and electrically compatible with Elite-C/nice!nano as much as possible.

It follows the [SparkFun Pro Micro RP2040](https://www.sparkfun.com/products/18288) pinout with 5 more pins (GPIO12-GPIO16) added along the bottom edge (like on Elite-C), and USB data lines broken out in the top corners (like nice!nano).

## Features

* Powerful dual-core Raspberry Pi RP2040 MCU
* 4 MB of on-board flash memory
* Only 3.2 mm thick thanks to a mid-mounted USB-C socket
* 500 mA linear regulator and resettable fuse
* Combined Pro Micro / Elite-C / nice!nano / SparkFun Pro Micro RP2040 compatible pinout
* 5 more I/O pins (GPIO12-GPIO16) added along the bottom edge 
* 23 total available digital pins for a maximum of 11x12 = 132 switches
* 4 pins configurable as analogue inputs
* USB D+/D- broken out for use with an external USB socket/daughterboard
* USB power sensing on GPIO19 for split keyboard side detection
* UF2 bootloader for drag & drop programming with no extra software required
* Orange indicator LED on pin GPIO17
* Now with [official CircuitPython support](https://circuitpython.org/board/42keebs_frood/)

## Availability

The Frood is now available from [42keebs.eu](https://42keebs.eu/shop/parts/controllers/frood-rp2040-pro-micro-controller/).

## Revision history

**Rev7** (23/06/2023)
* Use a different 4 MB flash chip (Winbond W25Q32JVUUIQ) which will hopefully not need a special config
* Use a higher-quality Panasonic reset/boot switches
* Some routing tweaks

**Rev6** (28/12/2022)
* Use a 4 MB (32 Mbit) flash chip (needs a special configuration in QMK `config.h`: `#define RP2040_FLASH_GD25Q64CS`)
* Tweak a few tracks

**Rev5** (26/10/2022)
* Improve USB socket position to match nice!nano
* Add BOOT/RESET pads on the bottom of the PCB (when the buttons are not accessible)
* Use a smaller crystal to gain some valuable space
* Add an orange indicator LED on pin GPIO17 (inspired by the [0xB2](https://github.com/plut0nium/0xB2))

**Rev4** (28/09/2022) - **Confirmed working**
* Use a 2 MB flash with correct supply voltage rating
* Switch to GT-USB-7014C USB-C socket and a standard 1.6 mm PCB
* Improve pin labels
* Improve routing

**Rev3** (18/08/2022) - **DO NOT USE!**
* Rename to "Frood"
* Use HRO-TYPE-C-31-M-14 for a fully mid-mounted socket with a 1.0 mm PCB
* Use 500 mA fuse instead of 350 mA one
* Improve layout (move USB termination resistors closer to MCU)
* Still uses the same flash chip with an incorrect supply voltage (1.8-2.6 V)

**Rev2** (16/08/2022) - **DO NOT USE!**
* Rename to "PiMicro2040"
* Fix crystal routing
* Use Elite-C/nice!nano-like outline
* Use mid-mounted USB-C connector (HRO-TYPE-C-31-M-13)
* Use a "standard" Sparkfun Pro Micro-compatible pinout
* Add 350 mA resettable fuse
* Add VBUS sensing
* Break-out USB data lines
* Contains a critical error - flash chip with an incorrect supply voltage (1.8-2.6 V)

**Rev1** (08/08/2022) - **DO NOT USE!**
* Initial version with a top-mounted USB-C socket, a shorter outline and a custom pinout
* Contains a critial error - incorrect crystal routing due to a mismatch between a 2-pin symbol and a 4-pin footprint
