# Mega328p_HV_resetter
clone and modification, original designed by https://mightyohm.com/files/hvrescue21/HVRescue_Shield_r21_schematic.png  

I have no MUN5311 but plenty of NPN transistors & resistors 220 / 1k / 10k lying around, so use whatever avaialble as it is, try NPN swtich as Tiny13_HV_resetter does, turns out that it works perfectely, 12V external supply is a must to be used.

1. burn the code the UNO   
2. connect pins to target MCU (Atmega328p)  
3. power up NANO    
4. turn on 12V supply  
5. press GO button
6. job done

### hardware design change  
NPN switch is an invertor, original author has design 5V->12V booster and the non-inverting control circuit thus the code was not working for my case. so the code has to change a bit.  

### software design change  
add routines,
VCC_on();
VCC_off();
RST_12V_on();
RST_12V_off();
