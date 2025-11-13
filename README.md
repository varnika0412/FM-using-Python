# FM-using-Python

Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program
```
import numpy as np
import matplotlib.pyplot as plt
Am=4.1
fm=343
fs=34300
Ac=8.2
fc=3430
t=np.arange(0,2/fm,1/fs)
B=4.2
m=Am*np.cos(2*np.pi*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c=Ac*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
s=Ac*np.cos((2*np.pi*fc*t)+B*np.sin(2*np.pi*fm*t))
plt.subplot(3,1,3)
plt.plot(t,s)
plt.tight_layout()
plt.show()
```
Output Waveform

![WhatsApp Image 2025-11-13 at 09 10 16_8bd0f052](https://github.com/user-attachments/assets/f05a4bec-f719-4a55-a65a-66e9f5ed8d60)



Tabular Column
![WhatsApp Image 2025-11-13 at 09 16 31_f5027410](https://github.com/user-attachments/assets/fbf3c6c1-d05b-4118-875e-6436bcab3cd7)




Calculation
![WhatsApp Image 2025-11-13 at 09 16 41_b161f5c9](https://github.com/user-attachments/assets/44843892-0835-495e-a309-4e202548c9b1)




Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
