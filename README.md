# PedalBoard-Alimentation
***
::: tip Table of contents
1. [230V Schematic](#230v-schematic)
2. [Diode Bridge Schematic](#diode-bridge-schematic)
3. [Regulated ouput Schematic](#regulated-output-schematic)
    1. [9V Output](#9v-output)
    2. [9-12V Output](#9-12v-output)
5. [10 Ouputs (7x9V +3x9-12V) Schematic and PCB](#10-ouputs-schematic)
6. [7 Outpout (7x9v) Schematic and PCB](#7_Output_Schematic_and_PCB)
7. [Kicad sources files](#Kicad_sources_files)
8. [Replicate Project](#replicate-project)
    1. [10 Outputs (7x9v + 3x9-12v) Version](#10-outputs-version)
    2. [7 Outputs (7x9v) Version](#7-outputs-version)
:::
***
## 230V Schematic
![230V Schematic](Images/Common/230VAC_part.png)
This is a basic schematic in order to protect your pedalboard against surges (VDR), short-circuit (fuse), electrical noise(EMI filter). You have to use at least a 230/12VAC transformer (best option because it causes less power dissipation on your regulators) and at most 230/18VAC transformer (you have to adapt this limit to your regulators specs). Keep in mind that after the diode brige the voltage is : 

![formula1](https://render.githubusercontent.com/render/math?math=\sqrt{2}\times%20U_{transformer})

For exemple this is the tension at the output of the diode bridge if your transformer ouput is 18V :

![formula1](https://render.githubusercontent.com/render/math?math=\sqrt{2}\times18\approx25.5V)

## Diode Bridge Schematic

![Diode Bridge Schematic](Images/Common/diode_bridge.png)

You connect each transformer outputs (if your transformer have only one secondary coil) on the "From-transformer-secondary-output_X" labels.
There are capacitors in parallel of each diodes to minimize noise from diodes. You have also a 2200µF capacitor to "smooth" the voltage from the diode bridge.
Finaly, you have a 1.85A polyfuse to protect your power supply and pedals mainly against short-circuits. All regulators are connected on "diodes bridge output".

## Regulated Output Schematic
Both regulations can be used in the same power supply. However keep in mind that you have to adapt transformer, diodes for the diodes bridge and polyfuse to the maximum current which can be used by your power supply (and add a margin of course).
### 9V Output
![9V output schematic](Images/Common/unit-9v.png)
The 4007 diode is used to prevent non-regulated voltage to go into your regulated voltage. C2 and C24 basicaly reduce noise from the regulator. The TVS diode protect your pedals against surges. I suggest to use 1A or 1.5A regulators to minimize thermal dissipation and to have an important margin ( specialy if you want to connect several pedals). Moreover, you have to had a heatsink to your regulator (a piece of aluminium should be enough).
### 9-12V Output
