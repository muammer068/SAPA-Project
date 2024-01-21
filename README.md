# SAPA-Project
Firstly, our project is an electronic stethoscope. The main idea of our project is to take the signals from some vital organs and analyze them. In this case, we can examine the project for two parts; taking the signals and analyzing the signals. First of all, we need to take voice with a physical instrument because it should collect the voice, especially from the exact area of the body. To achieve this we have used a usual stethoscope. Also, we know that it will collect some other signals that we don't want. We will name them as parasites. So in this situation, we need a circuit part for our project. The circuit will help us take the voice signal, filter it, and give some gain. If we want to hear the signals, we can add a speaker to the output. To get more clear signals, we used 2 different circuits for heartbeat and respiratory. Because these organs have different ranges of frequency. And we apply different types of filters to take them. We have used a lowpass filter for heartbeat and a bandpass filter for respiratory. The voltage of the signal without gain is around 15mV and we add a gain of 200 so that, the output voltage of the signal is around 3V. So far, we have collected the signal, filtered it, and the signal was gained. Secondly, we have to convert the analog signal to digital because we need to analyze the signals. We have used Arduino as an ADC. Through Arduino, the input voltages of analog signals are converted into digital data between 0 and 1023, which is a format that can be read and processed by other devices. Lastly, we show the raw, filtered, and FFT(fast Fourier transform) on GUI.
# Circuit Develop & Design
We developed two different circuits. Both of the circuits are supplied by 9V direct currents. Also, microphone and speaker components are the same for circuits. We used buffers to provide electrical impedance transformation between the circuits. For example between microphone circuits and filters. The Second Order Low Pass Sallen-Key filter with a cut-off frequency of around 200 Hz was implemented for the heart to effectively separate heart sounds from other organ noises. This filter highlights the fundamental frequency components of heart sounds that convey it while minimizing noise and hence can retain its original signal. In the same manner, bandpass filter cascaded low-pass plus high-pass Sallen-Key filters used for separation of lung sounds effectively isolated sound between 200-1000Hz. Thus, the distinction between heart and lung sounds is distinct. Lastly, to get a voice from the speaker we connected a speaker circuit with LM386EE opamp also provides a gain of 200 to signal. 

# Components for Heartbeat Circuit
•	1, 10k𝝮 resistor

•	3 ,4.7k𝝮 resistors

•	1 ,1k𝝮 resistor

•	1 ,10 𝝮 resistor

•	1 ,470µF capacitor

•	1 ,1000µF capacitor

•	2 ,220µF capacitors

•	1 ,10µF capacitor

•	3 ,100nF capacitors

# Schematic Design Of Heatbeat Circuit
![image](https://github.com/muammer068/SAPA-Project/assets/157306706/2b05e3ec-8af0-4caa-899d-d4ac12006039)

# Components for Respiratory Circuit
•	1, 4.7k𝝮 resistor

•	1 ,11k𝝮 resistors

•	2 ,1.5k𝝮 resistor

•	2 ,1.2k 𝝮 resistor

•	1 ,10k 𝝮 resistor

•	1 ,470µF capacitor

•	2 ,1µF capacitor

•	1 ,1000µF capacitor

•	2 ,220µF capacitor

•	2 ,100nF capacitor

•	1 ,10µF capacitor

# Schematic Design Of Respiratory Circuit
![image](https://github.com/muammer068/SAPA-Project/assets/157306706/43aa0406-3eec-466a-83e4-68b8dd36798a)

# Software | Setup & Capabilities
The software has been developed by using MATLAB's App Designer

# Monitoring and Processing Signals with the Help of Matlab and GUI Interface
This section gives information about the operations performed on Matlab and the GUI interface of sounds converted to digital signals with Arduino.

![image](https://github.com/muammer068/SAPA-Project/assets/157306706/4394ba9f-818c-49b8-be19-d4727e91d785)

Here are some capabilities of the interface;
1.	Allows the interface to be turned on/off
2.	Allows easy selection of the COM to which Aurdino is connected.
3.	It allows the processed data to be saved.
4.	It allows the recorded data to be printed to the desired location on the computer.
5.	The organ to be examined is selected.
6.	It allows the low pass frequency of the digital filter to be adjusted for the heart.
7.	Allows the low pass and high pass frequencies of the digital filter to be adjusted for the lung.
8.	Tells how many times the organ beats during the monitored period
9.	Shows the sound data coming from the organ.
10.	It shows the sound data coming from the organ after applying the digital filter.
11.	Shows the FFT version of the original signal.
12.	Shows the FFT version of the digitally filtered signal. 






