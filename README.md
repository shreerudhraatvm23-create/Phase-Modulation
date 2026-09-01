# Phase-Modulation

EXP NO:5 Phase Modulation using SCILAB

AIM:
To implement and analyze phase modulation (PM) using SCILAB

EQUIPMENTS REQUIRED:

•	Computer with i3 Processor

•	SCI LAB

THEORY:
Phase Modulation (PM) is a technique where the phase of the carrier wave is varied in proportion to the instantaneous amplitude of the input signal (message signal). Unlike frequency modulation, where the frequency is varied, in phase modulation, the phase angle of the carrier wave changes with the amplitude of the message signal.


The general form of a PM signal can be represented as:

<img width="816" height="464" alt="image" src="https://github.com/user-attachments/assets/e89dda9c-fc72-4335-9214-8fb96f4b32d7" />


ALGORITHM:

1.Initialize Parameters: Set the values of carrier amplitude, carrier frequency, message frequency, sampling frequency and phase deviation sensitivity.

2.Generate Time Axis: Create a time vector for the required signal duration using the sampling frequency.

3.Generate Message Signal: Generate the message signal as a cosine wave.

4.Generate Carrier Signal: Generate the carrier signal using the carrier amplitude and carrier frequency.

5.Generate PM Signal: Apply the phase modulation equation using the message and carrier signals to obtain the phase-modulated signal.

6.Plot the Signals: Plot the message signal, carrier signal and phase-modulated signal using Scilab plotting commands.

7.Display the Result: Observe the phase variation of the carrier signal according to the message signal.

PROGRAM:

clc;
clear;

t = 0:0.01:2*3.14;
x = sin(3*t);

subplot(3,2,1);
plot(x);

au = xcorr(x,x);

subplot(3,2,2);
plot(au);

v = fft(au);

subplot(3,2,3);
plot(abs(v));

fw = fft(x);

subplot(3,2,4);
plot(real(fw), imag(fw));

fw2 = (abs(fw)).^2;

subplot(3,2,5);
plot(fw2);


CALCULATION:

<img width="1080" height="1482" alt="WhatsApp Image 2026-09-01 at 9 46 35 PM" src="https://github.com/user-attachments/assets/35306314-24a4-473f-8fae-b56ad03750f1" />

<img width="899" height="1599" alt="WhatsApp Image 2026-09-01 at 9 46 35 PM (1)" src="https://github.com/user-attachments/assets/d5786008-e87c-46ea-aeb6-1f3262b4df13" />

TABULATION:

<img width="1599" height="899" alt="WhatsApp Image 2026-09-01 at 9 46 36 PM" src="https://github.com/user-attachments/assets/c25d9fc9-08d8-4487-bbcf-6291f2677ed9" />

RESULT:

The message signal, carrier signal, and phase-modulated (PM) signal will be displayed in separate plots. The modulated signal will show phase variations corresponding to the amplitude of the message signal.

