# Marlin 3D Printer Firmware for Creality CR-10 with MKS Gen L motherboard

## Creality CR-10 stock except
* Motherboard : MKS Gen L v1.0
* TMC2208 stepper drivers
    * X/Y/E = 0.9v
    * Z = 0.7v
    * Z2 = 0.7v
* Fang : https://www.thingiverse.com/thing:2763931 (file "FANG-oz-fang-5015.stl")
* BLTouch support : https://www.thingiverse.com/thing:2839373
* Dual Z (1 driver per Z motor)

## Simplify3D scripts

### Starting Script

```
G28 ; home
G34 ; Z stepper align (will G28 all axes)
G29 ; execute bed automatic leveling compensation
G1 X0 Y0 Z5 F1500 ; go to home
M104 S[extruder0_temperature] T0 ; set tool temperature
M109 S[extruder0_temperature] T0 ; wait for tool temperature
G1 X130 Y2 F1500 ; avoid binder clips
G1 Z0.2 F3000 ; get ready to prime
G92 E0 ; reset extrusion distance
G1 X170 E10 F600 ; prime nozzle
G1 X200 F5000 ; quick wipe
M900 K0.7 ; set K-factor
```

### Ending script

```
G1 X0 Y300 ; 
M106 S0 ; turn off cooling fan
M104 S0 ; turn off extruder
M140 S0 ; turn off bed
M84 ; disable motors
```

## Tutorials
[Z offset calibration with BLTouch](https://youtu.be/y_1Kg45APko)
