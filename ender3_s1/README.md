# Ender 3 S1

## Required slicer configuration

Since I use PrusaSlicer the following config snippets are only tested on that, but should be fairly easy to adapt to the slicer of your choosing.

### Start GCODE

```
M190 S0; don't set bed temperature
M104 S0; don't set extruder temperature
START_PRINT BED_TEMP=[first_layer_bed_temperature] EXTRUDER_TEMP={first_layer_temperature[initial_extruder]} AREA_START={first_layer_print_min[0]},{first_layer_print_min[1]} AREA_END={first_layer_print_max[0]},{first_layer_print_max[1]}
```

### End GCODE

```
END_PRINT
```

## Modifications

### Print bed

Due to a cable failure on the original I have replaced the stock print bed with the 3-point Y-carriage and heated bed from GulfCoast Robotics.
- [3-Point Y-carriage](https://gulfcoast-robotics.com/collections/products/products/modular-3-point-y-carriage-for-ender-3-s1-pro)
- [Build plate](https://gulfcoast-robotics.com/collections/heated-beds/products/aluminum-build-plate-and-24v-200w-silicone-heater-for-heated-bed-creality-ender-3)

### Print head

I have made the following changes to the stock print head:

- Creality 3D Heating Block Kit - High Temperature Pro (300℃) ([Creality store link](https://www.creality3dshop.eu/products/creality3d-heating-block-kit-high-temperature-pro-300-for-ender-3-s1-ender-3-s1-pro-cr-10-smart-pro-sermoon-v1-sermoon-v1-pro-hot-end))
- Brozzl Mk8 Copper plated 0.6mm nozzle ([3DJake link](https://www.3djake.com/brozzl/mk8-nozzle-copper-plated?sai=6179))

### Part cooling

<img src="../_assets/ender_3_s1_fan_duct_v3.png" width=33% height=33%>

I have replaced the stock part cooling fan with a GDSTIME 5015 24v blower fan. ([Amazon link](https://www.amazon.de/gp/product/B08QJ5C5PS))

In order to mount this I have purchased and installed V3 of this fan system by [Zuff](https://cults3d.com/en/users/Zuff): https://cults3d.com/en/3d-model/tool/air-duct-5015-ender-3-s1-pro-v3

### Hotend cooling

<img src="../_assets/ender_3_s1_support_plate.png" width=33% height=33%>

I have replaced the stock hotend cooling fan with a GDSTIME 5015 24v blower fan. ([Amazon link](https://www.amazon.de/gp/product/B08QJ5C5PS))

In order to mount this I have purchased and installed this support plate by [Zuff](https://cults3d.com/en/users/Zuff): https://cults3d.com/en/3d-model/tool/ender-3-s1-pro-4020-fan-cr-touch-no-y-offset. This has the additional benefit of removing the Y offset for the CR-Touch allowing it to reach more of the bed.

### Print bed

I have added some clips to the print bed to help align the PEI sheet. These are also designed by [Zuff](https://cults3d.com/en/users/Zuff): https://cults3d.com/en/3d-model/tool/creality-ender-3-s1-s1pro-guide-plaque-pei.

In order to be able to move the printer a bit further back towards the wall I have rotated the bed cable 90 degrees. I have used the following model to do so: https://www.thingiverse.com/thing:5408215.
I have also added this cable guide to prevent he cable from getting snagged on the stepper motor / Y-axis gantry: https://www.thingiverse.com/thing:5562309.
