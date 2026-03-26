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
clc;
clear;

// Parameters
Ac = 7.4;          // Carrier amplitude
Am = 3.7;          // Message amplitude
Fc = 1660;       // Carrier frequency (Hz)
Fm = 166;        // Message frequency (Hz)
Fs = 16600;      // Sampling frequency (Hz)

// Time axis
t = 0:1/Fs:2/Fm;

// Message signal
m = Am * sin(2*%pi*Fm*t);

// Carrier signal
c = Ac * sin(2*%pi*Fc*t);

// AM modulation
am_signal = (Ac + m) .* sin(2*%pi*Fc*t);

// Plotting
subplot(4,1,1);
plot(t, m);
title("Message Signal");
xgrid();

subplot(4,1,2);
plot(t, c);
title("Carrier Signal");
xgrid();

subplot(4,1,3);
plot(t, am_signal);
title("AM Modulated Signal");
xgrid();

// AM Demodulation using envelope detector
demodulated_signal = abs(hilbert(am_signal)) - Ac;

subplot(4,1,4);
plot(t, demodulated_signal);
title("Demodulated Signal");
xgrid();

```
Output:

![WhatsApp Image 2026-03-20 at 9 07 28 AM](https://github.com/user-attachments/assets/0f116eff-b83f-4660-8d73-8e2ba340bd6e)

Tabulation:

<img width="821" height="580" alt="image" src="https://github.com/user-attachments/assets/bf901d51-1f67-41f7-8435-2095b266a88f" />

Calculation:

<img width="770" height="686" alt="image" src="https://github.com/user-attachments/assets/f745e6be-4560-40ac-9d14-b726193e0939" />


Result:
RESULT: Thus the amplitude modulation and demodulation is experimentally done and the output is verified.
