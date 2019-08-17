# DC-27-Badge
The DC614 badge for DEF CON 27

## BOM

Note: Purchase links are "for example." You can often find better deals elsewhere, especially if you're willing to wait for shipping from China.

* 1x DC614 PCB
* 3x ??? Resistors
* 1x ??? LED
* 2x [1x13 female header rows](https://smile.amazon.com/2-54mm-Female-Single-Straight-Header/dp/B07SDDHZ34)
* 1x [MicroSDXC card (minimum 4 GB capacity)](https://smile.amazon.com/SanDisk-Professional-MicroSDXC-Hero-formatted/dp/9973399986/)
* 1x [Orange Pi Zero 512 MB](https://smile.amazon.com/Orange-Pi-Single-Board-Computer/dp/B0773HFXCY)
* 2x [Female USB-A ports](https://smile.amazon.com/TOVOT-Female-Connector-Mounting-Assortment/dp/B07569PK5B/)
* 1x [Ralink RT5370 with antenna](https://smile.amazon.com/Connecting-Wireless-Adapter-150Mbps-Raspberry/dp/B073J3HXZH)
* 1x [nRF24LU1p aka CrazyRadio with antenna](https://www.ebay.com/itm/Crazyradio-2-4Ghz-nRF24LU1-USB-radio-dongle-with-antenna-for-Crzayflie-10DOF/323793107106)
* 1x [LM2596 DC stepdown voltage regulator](https://smile.amazon.com/Adjustable-Converter-1-5-35v-Efficiency-Regulator/dp/B07C2QF1T1)
* 1x [LM386 audio amplifier](https://smile.amazon.com/5V-12V-Amplifier-Module-Arduino-EK1236/dp/B01FDD3FYQ/)
* 1x [28mm 8 ohm 1 watt speaker](https://smile.amazon.com/YXQ-Internal-Speaker-Magnet-Loudspeaker/dp/B07GFF9RKB)
* 2x [9v battery buckles](https://smile.amazon.com/uxcell-Battery-Connector-Leather-Housing/dp/B07BRRCBWY/)
* 2x [3D-printed 9v battery holders](https://www.thingiverse.com/thing:3364699)

## Preparation

* Carefully shuck the plastic from the RT5370 module so that it can comfortably fit behind the PCB.
* Following the [MouseJack instructions](https://github.com/BastilleResearch/mousejack), flash the [Nordic Semiconductor research firmware](https://github.com/BastilleResearch/nrf-research-firmware) to the nRF24LU1p/CrazyRadio.
* Using a voltmeter, calibrate the LM2596 to output 5V, then hot glue the potentiometer to avoid frying your Pi.

## Desoldering

1. TODO

## Surface-Mount Soldering

1. TODO

## Remaining Soldering

1. TODO

## Cleanup

1. TODO

## Creating the Boot Image

1. Use reconstruct.sh within the image directory to create the flashable .img.
2. You can then use something like balenaEtcher or dd to write the resulting .img to the MicroSDXC card (at least 4 GB).

## Final Steps

1. Insert the flashed MicroSDXC into the Pi.
2. Carefully seat the Pi so that its ethernet port faces downwards (towards the bottom of "Ohio").
3. Connect the Ralink RT5370 and nRF24LU1p with antennas attached to the soldered female USB-A ports.
4. Carefully connect at least one 9v battery to one of the buckles.
5. Some sounds occur doing boot; using a screwdriver, carefully adjust the potentiometer on the LM386 until you hear good sounding playback.
6. Enjoy your DC614 badge!

