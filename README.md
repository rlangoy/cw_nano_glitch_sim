# ChipWhisperer Nano glitch simulation using LT-SPICE



Simulation files for the [ Chipwisper Nano ](https://github.com/newaetech/chipwhisperer/blob/develop/hardware/capture/chipwhisperer-nano/NAE-CW1101-04_CWNANOSCH.pdf) glitct output to the glitched target

### Result of singe 60ns Pulse
#### FDN337N vs DMM3200U  (The model of DMM3200U is not correct (to low turn-off delay)
![alt text](https://github.com/rlangoy/cw_nano_glitch_sim/raw/main/images/VDD_GLITCH_OUTPUT_FDN337N_VS_DMM3200U.png)
#### FDN337N vs IRLML6246
![alt text](https://github.com/rlangoy/cw_nano_glitch_sim/raw/main/images/VDD_GLITCH_OUTPUT_FDN337N_VS_IRLM6246.png)
#### BSS214NW vs IRLML6246
![alt text](https://github.com/rlangoy/cw_nano_glitch_sim/raw/main/images/VDD_GLITCH_OUTPUT_BSS214NW_VS_IRLM6246.png)


### Result of multiple 60ns Pulse with 50% dutycycle (The model of DMM3200U is not correct (to low turn-off delay)
![alt text](https://github.com/rlangoy/cw_nano_glitch_sim/raw/main/images/VDD_GLITCH_OUTPUT_FDN337N_VS_DMM3200U_multiple_60ns_pulses.png)

### CW-Nano mod for sucessfully glitching the target
(Card has FDN337N and R12 = 20 Ohm ) - Adding a 5.6 Ohm resistor and opening Sj6 to grenerate aprox 600mV bias
![alt text](https://github.com/rlangoy/cw_nano_glitch_sim/raw/main/images/mod_glitch.png)
\

#### Simulation result: 
![alt text](https://github.com/rlangoy/cw_nano_glitch_sim/raw/main/images/vdd_glitch_sim.png)
#### Mesured result:
![alt text](https://github.com/rlangoy/cw_nano_glitch_sim/raw/main/images/mod_glitch_scope.png)


#### Glitching result from running : SOLN_Fault 2_1B - Introduction to Voltage Glitching with CWNano.ipynb 
https://github.com/newaetech/chipwhisperer-jupyter/blob/bef01d5b4d272d2c76c59afafc19f770c26ce0d7/courses/fault101/SOLN_Fault%202_1B%20-%20Introduction%20to%20Voltage%20Glitching%20with%20CWNano.ipynb


![alt text](https://github.com/rlangoy/cw_nano_glitch_sim/raw/main/images/Glitch_results.png)




#### LT-Spice can be downloaddet from: 
https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html 


#### Spice Models download: 
|   Model |URL                                                                                                                             |
|---------|  :-----------------------------------------------------------------------------------------------------------------------------|
|BSS214NW | https://www.infineon.com/dgdl/Infineon-SimulationModel_OptiMOS_PowerMOSFET_PSpice_20V_N-Channel-SimulationModels-v01_00-EN.zip?fileId=db3a304344ae06150144b733451709e2                                                         | 
|IRLM6246 | https://www.infineon.com/dgdl/irlml6246.spi?fileId=5546d462533600a40153573a9c3a3dd6 |
|DMN3200U | https://www.diodes.com/spice/download/1625/DMN3200U.spice.txt                       |
|FDN337n  | https://www.onsemi.com/download/models/lib/fdn337n.lib                              |



#### Datasheets 
https://www.infineon.com/dgdl/Infineon-BSS214NW-DS-v02_02-en.pdf?fileId=db3a30431b3e89eb011b695aebc01bde
https://www.infineon.com/dgdl/Infineon-IRLML6246-DataSheet-v01_01-EN.pdf?fileId=5546d462533600a40153566878f22621 \
https://www.diodes.com/assets/Datasheets/ds31188.pdf \
https://www.onsemi.com/pdf/datasheet/fdn337n-d.pdf 



