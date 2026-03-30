# Amplitude-Modulation-and-Demodulation-using-NumPy-and-Matplotlib-T1-C12-EVEN
Aim:

To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries.

Apparatus Required:

Software: Python with NumPy and Matplotlib libraries Hardware: Personal Computer

Theory:

Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting information via a radio carrier wave. In AM, the amplitude of the carrier wave is varied in proportion to that of the message signal. The general form of an AM signal is:

Algorithm:

Initialize Parameters: Set the values for carrier frequency, message frequency, and sampling frequency.
Generate Time Axis: Create a time vector for the signal duration.
Generate Message Signal: Define the message signal as a cosine wave.
Generate Carrier Signal: Define the carrier signal as a cosine wave.
Modulate Signal: Apply the AM formula to obtain the modulated signal.
Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program:

```
import numpy as np
import matplotlib.pyplot as plt


Am=3.7
fm=166
fs=16600
t=np.arange(0,2/fm,1/fs)
m=Am*np.cos(2*np.pi*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)

Ac=7.4
fc=1660
c=Ac*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)

am=(Ac+m)*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,3)
plt.plot(t,am)
plt.show()


```
Output:

<img width="1198" height="704" alt="image" src="https://github.com/user-attachments/assets/8f3a9c12-0ba3-4255-be7a-62b899bb7997" />


Tabulation:

<img width="821" height="580" alt="image" src="https://github.com/user-attachments/assets/bf901d51-1f67-41f7-8435-2095b266a88f" />


Result:
RESULT: Thus the amplitude modulation and demodulation is experimentally done and the output is verified.
