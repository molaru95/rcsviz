Benchtesting neural data playback 
==

Summary:
-------------
This document explains how to playback neural data using this setup: 

<INSERT PHOTO OF SETUP HERE... (images/hardware_demo.jpg)>

All necessary scripts to process digital neural data are also included in this document. 

Preprocessing neural data:
-------------
In MATLAB, add the RawDataTD.mat file to your workspace
Transform the data into an audio-compatible format using this MATLAB function:
<INSERT SCRIPT HYPERLINK HERE... (data/audioOut.m)>

Overview of the DAC setup:
-------------
The audio DAC has four output aux cables that feed into the copper Faraday cage and are then used as inputs for the circuit. 
Each aux cable contains two signal (white) and one ground (black) wire, which you can see inside of the Faraday cage.
The signal from the black wire travels directly to the RCS by conducting electricity through the copper RCS holder. 
**Important: The RCS must be inside the holder for the setup to be properly grounded.**

On the output end of the circuit, the rainbow colored wires send signal to the contacts of each lead. 
I've hooked the wires up so that aux cable 1 records from contacts 0-2, aux cable 2 records from contacts 1-3, and so on.

Using the DAC setup:
-------------
* Place the CTM inside the smaller compartment of the Faraday cage. You'll need to rotate the battery out for the CTM to fit. 
Note: There is a cardboard holder to rest the battery. 
* Connect the audio DAC to either a macOS or windows machine with a USB-C cord. 
* Minimize all unnecessary wiring on the computer connected to the audio DAC
**Important: Make sure the laptop is not charging **
* Recommended -- record for 5 minutes without playing data to make sure the setup is working properly.
Your FFT data should look something like this: 
<INSERT PHOTO OF FFT NOISE HERE... (images/fft_control.jpg)>
To create a graph like the one above, use MATLAB's `pspectrum` function

Summary checklist before collecting data:
-------------
* Check that all wires are securely connected
* Check that lead is making contact with metal spring
* Trace all wires to ensure proper data recording
* Avoid ground loops by minimizing any additional ground wires (don't charge your laptop while recording)
