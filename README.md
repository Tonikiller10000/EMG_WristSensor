# EMG WRIST SENSOR

## Description:
This project is an electromiography sensor witch can detect muscular activity. 

<img src="https://github.com/Tonikiller10000/EMG_WristSensor/blob/main/EMG_P3.png"/>
<img src="https://github.com/Tonikiller10000/EMG_WristSensor/blob/main/EMG_P2.jpg"/>
<img src="https://github.com/Tonikiller10000/EMG_WristSensor/blob/main/EMG_P1.jpg"/>


## Abandoned project
After making the PCB, when working at the software, I found about it`s limitations.
With EMG(electromiography) you can detect the voltage produced by the muscle contraction, meaning that for you to recive a signal, you need to stay with the muscle contracted. 
For exemple, closing your hand into a relaxed fist will not generate signals, unless you clench it, and you will recive a electrical voltage(mV).
When you feel a touch the senzation goes trouth the nerves(deeper) rather than muscles with a weeker signal detectable only with needles.
The input is not verry precise at all, and is verry tiering to stay with the muscle contracted for a long time.

> [!WARNING]
> !!! do not use needles... it can cause infections, blood electrolisis, metal poisoning and other health risks.

Detected actions: 
- relaxed palm
- tigth fist
- extended palm 
- wrist movements up/down
- snap
- press
- other...

<img src="https://github.com/Tonikiller10000/EMG_WristSensor/blob/main/EMG_SerialPlotter.png"/>

## How it works
- it has 6 pairs of diferential op amps each with a variable gain potentiometer. (it removes the 50-60hz noice from the grid) (all differential op amps have a common offset potentiometer)
- each output goes trouth an op amp with another gain potentiometer, and then It goes to an STM ADC pin
- teh data is scanned and sent to the usb virtual port and can be read with a plotter
- when using it, connect the gnd to the skin so it dosen`t stay floating and produce electrostatis shots.
- !!! when programming with a STLINK, power it via the usb and disconnect the power from stlink to stm (keep the gnd)

## Future
I will use the sensors in the future to calculate precise data

## Links:
74HC595 datasheet (shift register): https://datasheetspdf.com/pdf-file/446162/ONSemiconductor/74HC595/1
AT28C256 datasheet (32K EEPROM): https://ww1.microchip.com/downloads/en/DeviceDoc/doc0006.pdf
AT28C64 datasheet (8K EEPROM): https://ww1.microchip.com/downloads/en/devicedoc/doc0001h.pdf
Online serial plotter: https://web-serial-plotter.atomic14.com/


