# Phase-Modulation

# Amplitude-Modulation

# EXP NO: 4	GENERATION AND DETECTION OF FM

## AIM:

To write a program for Phase Modulation and Demodulation using SCILAB.

## EQUIPMENTS REQUIRED

•	Computer with i3 Processor

•	SCI LAB

## THEORY:

Pha modulation is a type of modulation in which the frequency of the high frequency (carrier) is varied in accordance with the instantaneous value of the modulating signal.

FREQUENCY DEVIATION Df and MODULATION INDEX m f :

The frequency deviation Df represents the maximum shift between the modulatedsignal

frequency, over and under the frequency of the carrier.


We define modulation index m f the ratio between Df and the modulating frequency

m= Df / fm

### Note: Keep all the switch faults in off position

FREQUENCY MODULATION GENERATION:

The circuits used to generate a frequency modulation must vary the frequency of a high frequency signal (carrier) as function of the amplitude of a low frequency signal (modulating signal). In practice there are two main methods used to generate FM.

## Algorithm:
1. Define Parameters:

· Fs: Sampling frequency.

· T: Duration of the signal.

· Fc: Carrier frequency.

· Fm: Frequency of the modulating signal.

· Beta: Modulation index, which controls the extent of frequency deviation.

2. Generate Signals:

· modulating_signal: Sinusoidal signal used for modulation.

· carrier_signal: The high-frequency carrier signal.

· modulated_signal: FM modulated signal calculated by varying the carrier frequency according to the modulating signal.

3. FM Modulation:

· Modulated_signal is obtained by modulating the carrier signal with the modulating signal.

4. FM Demodulation:

· Differentiation: Computes the derivative of the modulated signal to extract frequency variations.

· Envelope Detection: Takes the absolute value to retrieve the envelope of the signal.

· Low-pass Filtering: Applies a Butterworth low-pass filter to smooth the envelope and recover the original modulating signal.

5. Visualization:

· Plots the modulating signal, carrier signal, FM modulated signal, and demodulated signal for analysis.

## Program
```
Am = 14.15;
fm = 1907;
Ac = 21.23;
fc = 19070;
fs = 190700;
t  = 0:1/fs:2/fm;
B = 4.9

em = Am*cos(2*%pi*fm*t);
subplot(3,1,1);
plot(t,em);

ec = Ac*cos(2*%pi*fc*t);
subplot(3,1,2);
plot(t,ec);


efm = Ac*cos(2*%pi*fc*t + B*sin(2*%pi*fm*t));
subplot(3,1,3);
plot(t,efm);

```


## Output Waveform:
<img width="1918" height="1197" alt="image" src="https://github.com/user-attachments/assets/22642096-20f3-4985-856b-0012acb954b8" />




## RESULT:
Thus the frequency modulation and demodulation is successfully done and the output is experimentally verified.
