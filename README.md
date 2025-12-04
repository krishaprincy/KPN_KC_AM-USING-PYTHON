# AM-using-Python

Aim

To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Amplitude Modulation (AM) is a method of transmitting information using a carrier wave by varying its amplitude in proportion to the instantaneous amplitude of the input (message) signal, while the frequency and phase remain constant.


Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate AM Signal: Apply the AM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program
```
import numpy as np
import matplotlib.pyplot as plt

Am = 2.6
fm = 154
Ac = 5.2
fc = 1540
fs = 15400

t = np.arange(0, 2/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)
c = Ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, c)
s = (Ac + m) * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 3)
plt.plot(t, s)
```

Output Waveform

<img width="932" height="652" alt="image" src="https://github.com/user-attachments/assets/f2b2759a-81a3-4c01-b14b-420a0153d928" />


Tabular Column

![WhatsApp Image 2025-12-04 at 15 38 34_ad8f101b](https://github.com/user-attachments/assets/da97f2d2-2f76-4af3-97e6-e083616aaba0)





Result

The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. The modulated signal will show amplitude variations corresponding to the amplitude of the message signal.
