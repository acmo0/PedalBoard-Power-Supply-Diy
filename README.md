# PedalBoard-Alimentation
***
# Table of contents
1. [230V Schematic](#230v-schematic)
2. [10 Ouputs (7x9V +3x9-12V) Schematic and PCB](#10_Ouputs_Schematic) 
3. [7 Outpout (7x9v) Schematic and PCB](#7_Output_Schematic_and_PCB)
4. [Only One ouput Schematic](#Schematic_of_one_output)
5. [Kicad sources files](#Kicad_sources_files)
6. [Replicate Project](#replicate-project)
    1. [10 Outputs (7x9v + 3x9-12v) Version](#10-outputs-version)
    2. [7 Outputs (7x9v) Version](#7-outputs-version)
***
## 230V Schematic
![230V Schematic](Images/Common/230VAC_part.png)
This is a basic schematic in order to protect your pedalboard against surges (VDR), short-circuit (fuse), electrical noise(EMI filter). You have to use at least a 230/12VAC transformer (best option because it causes less power dissipation on your regulators) and at most 230/18VAC transformer (you have to adapt this limit to your regulators specs). Keep in mind that after the diode brige the voltage is : 

![formula1](https://render.githubusercontent.com/render/math?math=\sqrt{2}\times%20U_{transformer})

For exemple if your transformer ouput is 18V you have :

![formula1](https://render.githubusercontent.com/render/math?math=\sqrt{2}\times18\approx25.5V)
