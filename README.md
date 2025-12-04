# DSBSC-USING-PYTHON

## AIM:

To implement and analyze DSBSC using Python's NumPy and Matplotlib libraries.
## EQUIPMENTS REQUIRED

   Software: Python with NumPy and Matplotlib libraries
   Hardware: Personal Computer

## Algorithm:

   1  Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
   2  Generate Time Axis: Create a time vector for the signal duration.
   3  Generate Message Signal: Define the message signal as a cosine wave.
   4 Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
   5 Generate DSBSC Signal: Apply the DSBSC formula to obtain the modulated signal.
   6 Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.
 ## PROGRAM
   ```
import numpy as np
import matplotlib.pyplot as plt

Am=7.6
fm=648
fc=6480
fs=64800
t=np.arange(0,2/fm,1/fs)
m=Am*np.cos(2*np.pi*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
Ac=12.4
c=Ac*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
s1=(Ac+m)*np.cos(2*np.pi*fc*t)
s2=(Ac-m)*np.cos(2*np.pi*fc*t)
s=s1-s2
plt.subplot(3,1,3)
plt.plot(t,s)
plt.show()
```
## OUTPUT WAVEFORM
<img width="555" height="416" alt="Screenshot 2025-12-04 124737" src="https://github.com/user-attachments/assets/333bc022-5c41-4a87-bf2c-d1ff1d73b493" />

## TABLE

## RESULT
Thus the DSB-SC-AM Modulation is generated using python.

