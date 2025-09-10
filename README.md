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
Am=6.9
Ac=13.8
Fm=539
Fc=5390
Fs=53900
b=2.5
t=np.arange(0,2/Fm,1/Fs)
m=Am*np.cos(2*np.pi*Fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c=Ac*np.cos(2*np.pi*Fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
s= Ac*np.cos(2*np.pi*Fc*t + b * np.sin(2*np.pi*Fm*t))
plt.subplot(3,1,3)
plt.plot(t,s)
```


Output Waveform
<img width="837" height="568" alt="image" src="https://github.com/user-attachments/assets/94dd3901-cca8-4999-9351-57488f2802b9" />



Tabular Column



Calculation




Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
