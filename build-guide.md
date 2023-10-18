# Build Guide

The Big Knob a 3d printed knob!

## Parts

### Required

| Name | Count | Remarks         |
| :-   | :-    | :-              |
| PCB  | 1     | [Gerber here](https://github.com/Jpe230/big_knob/blob/main/PCB/GERBER_PCB_Big_Knob.zip) |
| RP2040 Pro Micro | 1 | See notes
| EC11 Encoder | 1 |             |
| WS2812B | 10 |                 |
| ST7735 80x160 (0.06inch)| 1 | [Screen used](https://aliexpress.com/item/1005005334510897.html) |
| Top case | 1 | [Link here](https://github.com/Jpe230/big_knob/blob/main/Case/stl/top_case.stl)|
| bottom plate | 1 | [Link here](https://github.com/Jpe230/big_knob/blob/main/Case/stl/bottom_plate.stl)|
| Diffuser | 1 | [Link here](https://github.com/Jpe230/big_knob/blob/main/Case/stl/diffuser.stl)|
| Knob | 1 | [Link here](https://github.com/Jpe230/big_knob/blob/main/Case/stl/knob.stl)|
| 8mm M3 screw | 4 ||
| 10mm M3 thread insert | 4 ||
| 4mm M2 screw | 4 ||
| M2 nut | 4 ||

#### Notes

Any RP2040 with a pro micro footprint should work, but the firmware must be modified, I used a Sparkfun PM2040

## Building

### Soldering the LEDS

The leds should be soldered with the arrow facing the bottom-right corner

### Soldering the Encoder

Remove the grounding tabs at the side of the cncoder and solder it

### Soldering the RP2040

The RP2040 should be mounted facing down.

### Soldering the Screen

With some thin wire solder the adjacent pads with the corresponding pad on the PCB.

## Mounting

1) Insert the screen into the slot of the top case
2) Insert the top 2 screws from the front and secure the screws with nuts
3) Insert the PCB into the top case
4) Insert the remaining screws to the designated holes and secure them with nuts.
5) Attach the bottom plate and secure it the M3 screws.

## Flashing

To compile the firmware please use QMK:

```
qmk compile -kb jpe230/big_knob -km default
```



