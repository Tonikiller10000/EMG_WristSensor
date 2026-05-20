# EMG WRIST SENSOR


## Description (Deprecated)
<b>This is an electromiography sensor witch can detect muscular activity.</b> 

After making the PCB, when working at the software, I found about it`s limitations.
With EMG(electromiography) you can detect the voltage produced by the muscle contraction, meaning that for you to recive a signal, you need to stay with the muscle contracted. 
For exemple, closing your hand into a relaxed fist will not generate signals, unless you clench it, and you will recive a electrical voltage(mV).
When you feel a touch the senzation goes trouth the nerves(deeper) rather than muscles with a weeker signal detectable only with needles.
The input is not verry precise at all, and is verry tiering to stay with the muscle contracted for a long time.

> [!WARNING]
> !!! do not use needles... it can cause infections, blood electrolisis, metal poisoning and other health risks.


<table>
  <tr>
    <td>
      <img src="https://github.com/Tonikiller10000/EMG_WristSensor/blob/main/EMG_P3.png" height="350" alt="3D Render">
    </td>
    <td>
      <img src="https://github.com/Tonikiller10000/EMG_WristSensor/blob/main/EMG_P2.jpg" height="350" alt="Physical Board">
    </td>
  </tr>
</table>
 


<table>
  <tr>
    <td>
        <h3>Detected actions:</h3>
        <ul style="list-style-type: none; padding-left: 20px;">
            <li> relaxed palm</li>
            <li> tigth fist</li>
            <li> extended palm</li>
            <li> wrist movements up/down</li>
            <li> snap</li>
            <li> press</li>
            <li> other...</li>
        </ul>
    </td>
    <td>
        <p align="center">
            <img src="https://github.com/Tonikiller10000/EMG_WristSensor/blob/main/EMG_SerialPlotter.png" width="550" alt="Image description">
        </p>
    </td>
  </tr>
</table>



<table>
  <tr>
    <td>
        <h3> HARDWARE MISTAKES & OBSERVATIONS</h3>
        <ul style="list-style-type: none; padding-left: 20px;">
            <li> 1.5K resistor to USB D+</li>
            <li> wrong RGB footprint</li>
            <li> STM32 code not uploaded</li>
        </ul>
    </td>
    <td>
        <p align="center">
            <img src="https://github.com/Tonikiller10000/EMG_WristSensor/blob/main/EMG_P1.jpg" width="300" alt="Image description">
        </p>
    </td>
  </tr>
</table>





## How it works & user instructions
- it has 6 pairs of diferential op amps each with a variable gain potentiometer. (it removes the 50-60hz noice from the grid) (all differential op amps have a common offset potentiometer)
- each output goes trouth an op amp with another gain potentiometer, and then It goes to an STM ADC pin
- then data is scanned and sent to the usb virtual port and can be read with a plotter
- when using it, connect the gnd to the skin so it dosen`t stay floating and produce electrostatis shots.
- !!! when programming with a STLINK, power it via the usb and disconnect the power pin from stlink to stm (keep the gnd common reference)
- use an [Online serial plotter](https://web-serial-plotter.atomic14.com/) or [Serial Studio Pro](https://serial-studio.com/) to see the USB data.
- More papers on the subject at [BioSignals Detection Documents folder](https://github.com/Tonikiller10000/EMG_WristSensor/tree/main/BioSignalsDetectionDocuments) 




