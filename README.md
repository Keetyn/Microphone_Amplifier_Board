# Microphone_Amplifier_Board

This is an audio amplifier board capable of taking any small audio signal, differential or singled ended and amplifying it to an output of 30W @ 8 ohms. This was designed, built, and tested as more of an educational exercise than anything else and thus relies on screw terminal inputs for power and requires external power supplies. 

The board can be thought of as having four distinct sections:

1. the first is a THAT 1510 instrumentation amplifier with a tunable gain that is meant to take in a signal       from either a microphone or an aux cord. This amplifies the signal by a gain of anywhere from +32 - +62dB      depending on the position of the gain potentiometer. This input can accept a differential or single    
   ended input.
2. The second is the EQ filter. This is a state variable topology filter. This implementation provides         
   potentiometers that allow the user to adjust the damping (alpha), Center Frequency (Fo), Gain (A), and a 
   latching pushbutton that can enable or disable the filter. Fo can be adjusted from 300Hz - 2.2kHz.             alpha can be adjusted from 0.5 - 10. Gain can be adjusted from -40dB - +15dB
3. The third is a Peak Limiter using a THAT 4305 Compander IC. This is a versatile analog processing IC that with the accompanying circuitry and potentiometers acts as a non-distorting peak limiter with the ability to adjust the compression threshold and compression ratio. The threshold can be adjusted from +7.3dBV - +9.74dBV. The compression ratio can also be adjusted anywhere from infinity:1 to a value approaching 1:1.
4. THe final section of this board is a TPA3122 Class-D analog input power amplifier. This IC is capable of outputting 30W and has an accompanying potentiometer that can be used to attenuate its input as a volume control.

<img width="1160" alt="Microphone_Amplifier_Flowchart" src="https://github.com/user-attachments/assets/4f5a4882-59a9-4e23-ba5c-568a937e7117">

Each of the above listed sections is split apart by 100 mil pin headers that completely break any connection between the sections. This was done for easier test and troubleshooting and to help compartmentalize individual portions of the board. Below is a screenshot of a 3D render of the board in KiCad with each section clearly separate with silkscreen lines and labels.

![KiCad_PCB_Render](https://github.com/user-attachments/assets/36a9d9fe-a775-4042-94ba-dfea9b36994f)

