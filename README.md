# SIMULATION-OF-AUTOCORRELATION-AND-PSD-USING-SCILAB-
## AIM
Write a program for Autocorrelation and PSD of signals in SCILAB and verify Wiener-Khinchin relation.

## EQUIPMENTS NEEDED

•	Computer with i3 Processor
•	SCI LAB

## THEORY
The Wiener-Khinchin theorem states that the power spectral density of a wide sense stationary random process is the Fourier transform of the corresponding autocorrelation function.
<img width="582" height="91" alt="image" src="https://github.com/user-attachments/assets/dacf7cfd-96c5-45a6-aa31-321978d15f97" />

## ALGORITHM
1.	Load or Define the Signal: Input your time-domain signal.
2.	Compute Autocorrelation: Calculate the autocorrelation function of the signal.
3.	Compute Power Spectral Density (PSD): Estimate the PSD of the signal, either directly using a method like Welch’s periodogram or by using the Fourier transform of the autocorrelation.
4.	Plot Results: Visualize the autocorrelation function and PSD.

## PROCEDURE

•	Refer Algorithms and write code for the experiment.

•	Open SCILAB in System

•	Type your code in New Editor

•	Save the file

•	Execute the code

•	If any Error, correct it in code and execute again

•	Verify the generated waveform using Tabulation and Model Waveform

## PROGRAM:
```
clc;
clear all;

// Time vector
t = 0:0.01:2*%pi;

// Input signal
x = sin(2*t);

// Plot original signal
subplot(3,2,1);
plot(x);
title("Original Signal");

// Autocorrelation
au = xcorr(x, x);
subplot(3,2,2);
plot(au);
title("Autocorrelation");

// FFT of Autocorrelation (PSD using Wiener-Khinchin theorem)
v = fft(au);
subplot(3,2,3);
plot(abs(v));
title("FFT of Autocorrelation (PSD)");

// FFT of original signal
fw = fft(x);
subplot(3,2,4);
plot(fw);
title("FFT of Signal");

// Power Spectral Density (|X(f)|^2)
fw2 = (abs(fw)).^2;
subplot(3,2,5);
plot(fw2);
title("Power Spectral Density (|X(f)|^2)");
```
## OUTPUT:
<img width="610" height="460" alt="516206835-bdd6d172-eb35-4c7d-a71d-80496b451b15" src="https://github.com/user-attachments/assets/4c9511d2-2719-4587-8cbb-62df0d787112" />

## RESULT:
Thus the Autocorrelation and PSD are executed in Scilab and output is verified.
