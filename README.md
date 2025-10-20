# FM-using-python

EX NO:7 DETECTION AND GENERTION OF USING PYTHON

AIM:
To write a program for Frequency Modulation and Demodulation using COLAB and to observe and measure the frequency deviation and the modulation index of FM.

EQUIPMENTS REQUIRED

• Computer with i3 Processor

• SCI LAB

Frequency modulation is a type of modulation in which the frequency of the high frequency (carrier) is varied in accordance with the instantaneous value of the modulating signal. FREQUENCY DEVIATION f and MODULATION INDEX m f : The frequency deviation f represents the maximum shift between the modulatedsignal frequency, over and under the frequency of the carrier.

We define modulation index m f the ratio between f and the modulating frequency m= f / fm

FREQUENCY MODULATION GENERATION: The circuits used to generate a frequency modulation must vary the frequency of a high frequency signal (carrier) as function of the amplitude of a low frequency signal (modulating signal). In practice there are two main methods used to generate FM. Algorithm

Define Parameters: • Fs: Sampling frequency. • T: Duration of the signal. • Fc: Carrier frequency. • Fm: Frequency of the modulating signal. • Beta: Modulation index, which controls the extent of frequency deviation.

Generate Signals: • Modulating signal: Sinusoidal signal used for modulation. • Carrier signal: The high-frequency carrier signal. • Modulated signal: FM modulated signal calculated by varying the carrier frequency according to the modulating signal.

FM Modulation: • Modulated signal is obtained by modulating the carrier signal with the modulating signal.

FM Demodulation: • Differentiation: Computes the derivative of the modulated signal to extract frequency variations. • Envelope Detection: Takes the absolute value to retrieve the envelope of the signal. • Low-pass Filtering: Applies a Butterworth low-pass filter to smooth the envelope and recover the original modulating signal.

Visualization: • Plots the modulating signal, carrier signal, FM modulated signal, and demodulated signal for analysis.

<img width="1000" height="500" alt="image" src="https://github.com/user-attachments/assets/7a21d2f5-a096-49fc-b56e-54b6fff4047c" />

PROGRAM:
```
import numpy as np
import matplotlib.pyplot as plt
Am=2.17
fm=264
fs=264000
Ac=3.17
fc=2640
b=2.9
t=np.arange(0,2/fm,1/fs)
m=Am*np.cos(2*3.14*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c=Ac*np.cos(2*3.14*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
Fm=Ac*np.cos((2*3.14*fc*t)+b*np.sin(2*3.14*fm*t))
plt.subplot(3,1,3)
plt.plot(t,Fm)
plt.tight_layout()
plt.show()
```
OUTPUT WAVEFORM:

<img width="700" height="500" alt="image" src="https://github.com/user-attachments/assets/3b6bce8b-77c7-4ec1-ba5b-d806c2ed84da" />

TABULATION:

<img width="800" height="1300" alt="image" src="https://github.com/user-attachments/assets/d215510d-5a63-4c1d-b7f3-8e307845cf10"/>

CALCULATION:

<img width="900" height="1000" alt="image" src="https://github.com/user-attachments/assets/bc2e2846-bee5-4daa-ac28-b420408de03a" />

Frequency Deviation Practical = 834

Modulation Index Practical = 3.1

Modulation Index Theoretical =2.9

RESULT:

Thus, the frequency modulation and demodulation is successfully done and the output is experimentally verified.

