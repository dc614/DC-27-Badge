# DC-27-Badge
The DC614 badge for DEF CON 27

## BOM

Note: Purchase links are "for example." You can often find better deals elsewhere, especially if you're willing to wait for shipping from China.

* 1x DC614 PCB (see `pcb/`)
* 3x 1206 82ohm Resistors
* 1x [Everlight Elec 67-23/R6GHBHC-B01/2T](https://lcsc.com/product-detail/Others_Everlight-Elec-67-23-R6GHBHC-B01-2T_C264607.html) (SMD-3.5X2.8X1.9(4P)) LED
* Assorted [male header pins](https://smile.amazon.com/Bestsupplier-Single-2-54mm-Header-Connector/dp/B0716BFCQ4/)
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

## Supplies and Equipment

### Preparation/Misc

* [Hot glue gun with glue](https://smile.amazon.com/Blusmart-Upgraded-Temperature-Projects-Artistic/dp/B01LW8UVYJ/)
* [Voltmeter](https://smile.amazon.com/INNOVA-3320-Auto-Ranging-Digital-Multimeter/dp/B000EVYGZA/)
* [Screwdriver](https://smile.amazon.com/Precision-Screwdriver-Flathead-Different-Electronic/dp/B07TDGXV5H/)
* [Pliars](https://smile.amazon.com/AmazonBasics-Plier-Tools-Set/dp/B015X2NHOK/)
* [Wire cutters/strippers](https://smile.amazon.com/VISE-GRIP-Stripping-Cutter-8-Inch-2078309/dp/B000JNNWQ2/)
* [Dykes](https://smile.amazon.com/VISE-GRIP-Diagonal-Cutting-Pliers-2078306/dp/B000A0S4YO/)
* [Gorilla Super Glue gel or similar](https://smile.amazon.com/Gorilla-Super-Glue-Gram-Clear/dp/B00OAAUAX8/)

### Soldering

* [Soldering iron](https://smile.amazon.com/gp/product/B00M1O9ZSG/) (and a [soldering iron tip cleaner](https://smile.amazon.com/Hakko-599B-02-Wire-type-soldering-cleaner/dp/B00FZPGDLA/) if possible)
* [Lead based rosin core solder](https://smile.amazon.com/MAIYUM-63-37-Solder-Electrical-Soldering/dp/B076QF1Y85)
* [Flux](https://smile.amazon.com/MG-Chemicals-milliliters-Pneumatic-Dispensing/dp/B00425FUW2/)
* [Soldering microscope](https://smile.amazon.com/Microscope-Soldering-Magnifier-Adjustable-Rechargeable/dp/B076KPGK2J/) (if possible)
* [Hot air station](https://smile.amazon.com/Tek-Motion-Display-Soldering-Station/dp/B01MR2IWBN/) (if possible)
* [Solder wick](https://smile.amazon.com/Tabiger-Solder-Desoldering-Sucker-Remover/dp/B0777LMVTT/)

### Cleaning

* [Powder-free nitrile gloves](https://smile.amazon.com/AMMEX-GPNB46100-BX-GlovePlus-Disposable-Industrial/dp/B004BR8KB4)
* [Soft bristle toothbrushes](https://smile.amazon.com/Oral-B-Bristles-Indicator-Contour-Toothbrush/dp/B06XK5MQG5/)
* [Isopropyl alcohol](https://smile.amazon.com/Amazon-Brand-Isopropyl-Antiseptic-Technical/dp/B07NFSFBXQ/)
* [Paper towels](https://smile.amazon.com/Amazon-Brand-Flex-Size-Regular/dp/B074CTW469/)
* [Lens cleaning wipes](https://smile.amazon.com/Care-Touch-Moistened-Cleansing-Eyeglasses/dp/B01NCOUY05/)

## Preparation

* Purchase/order a DC614 PCB (see `pcb/`)
* Carefully shuck the plastic from the RT5370 module so that it can comfortably fit behind the PCB.
* Following the [MouseJack instructions](https://github.com/BastilleResearch/mousejack), flash the [Nordic Semiconductor research firmware](https://github.com/BastilleResearch/nrf-research-firmware) to the nRF24LU1p/CrazyRadio.
* Using a voltmeter, calibrate the LM2596 to output 5V, then hot glue the potentiometer to avoid frying your Pi.

## Desoldering

### LM386

1. Desolder the speaker wire holder (connector at the end) from the LM386.
2. Desolder the 4 header pins from the other end of the LM386, carefully leaving the holes clean for reuse.

### Pi

1. Desolder the 13 header pins from the Orange Pi Zero, carefully leaving the holes clean for reuse.

## Surface-Mount Soldering

1. Solder the resistors and LED into their respective places on the face of the board.

## Remaining Soldering

1. Solder 13 header pins to the one-row side of the Orange Pi Zero, facing opposite in orientation to the original header row (the Pi will mount with its back facing the back of the board).
2. Solder 13 header pins to the inner row of the opposite side of the Orange Pi Zero, in the same orientation as the other row.
3. Solder a 13 pin female header row on the back of the board on the one-row side.
4. Solder a 13 pin female header row on the back of the board on the innermost opposite side.
5. Solder two female USB connectors to the back of the board, oriented so that devices plug in in parallel to the board.
6. Using 4 header pins, solder the LM2596 to the board.
7. Using 4 header pins, solder the LM386 to the board.
8. Solder the speaker directly to the LM386, and pin it in place with header pins.
9. Solder the battery buckles above the LM2596 (ground on the right if the back of the board is facing you).

## 3D Printing

1. Slice and print the battery carriers.
2. Using glue, attach battery carriers next to pi.

## Cleanup

Using nitrile gloves, isopropyl alcohol, paper towels, and a soft-bristled toothbrush, clean any remaining flux from the PCB and gently wipe and buff the front surface of the board. Use lens cleaning cloths for stubborn sticky spots.

## Creating the Boot Image

1. Within the `image` directory, run `reconstruct.sh` to create the flashable `.img`.
2. Use [balenaEtcher](https://www.balena.io/etcher/) (or `dd`) to write the resulting `.img` to the MicroSDXC card.

## Final Steps

1. Insert the flashed MicroSDXC into the Pi.
2. Carefully seat the Pi so that its ethernet port faces downwards (towards the bottom of "Ohio").
3. Connect the Ralink RT5370 and nRF24LU1p with antennas attached to the soldered female USB-A ports.
4. Carefully connect at least one 9v battery to one of the buckles.
5. Some sounds occur during boot; using a screwdriver, carefully adjust the potentiometer on the LM386 until you hear good sounding playback.
6. Enjoy your DC614 badge!
