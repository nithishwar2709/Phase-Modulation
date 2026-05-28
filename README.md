# Phase-Modulation

# EXP NO: 7	GENERATION AND DETECTION OF PM

## AIM:

To write a program for Phase Modulation and Demodulation using SCILAB.

## EQUIPMENTS REQUIRED

•	Computer with i3 Processor

•	SCI LAB

## THEORY:

## PHASE MODULATION (PM):

Phase modulation is a type of modulation in which the phase of the high frequency (carrier) signal is varied in accordance with the instantaneous value of the modulating signal.

### PHASE DEVIATION (Δθ) AND MODULATION INDEX (mp):

The phase deviation Δθ represents the maximum change in phase of the carrier signal caused by the modulating signal.

We define the modulation index mp as the ratio of phase deviation to the amplitude of the modulating signal.

mp = Δθ

(Phase modulation index is measured in radians.)

### Note:
Keep all the switch faults in OFF position.

## PHASE MODULATION GENERATION:

The circuits used to generate phase modulation must vary the phase of a high frequency signal (carrier) as a function of the amplitude of a low frequency signal (modulating signal). In practice, different methods are used to generate PM signals.

## Algorithm:1. Define Parameters:

· Fs: Sampling frequency.

· T: Duration of the signal.

· Fc: Carrier frequency.

· Fm: Frequency of the modulating signal.

· Mp: Phase modulation index, which controls the extent of phase deviation.

2. Generate Signals:

· modulating_signal: Sinusoidal signal used for modulation.

· carrier_signal: The high-frequency carrier signal.

· modulated_signal: PM modulated signal calculated by varying the phase of the carrier signal according to the modulating signal.

3. Phase Modulation:

· modulated_signal is obtained by phase modulating the carrier signal with the modulating signal.

4. Phase Demodulation:

· Phase Detection: Extracts the phase variations from the PM signal.

· Envelope Detection: Takes the absolute value to retrieve the envelope of the signal.

· Low-pass Filtering: Applies a Butterworth low-pass filter to smooth the signal and recover the original modulating signal.

5. Visualization:

· Plots the modulating signal, carrier signal, PM modulated signal, and demodulated signal for analysis.

## Program
```
Am = 15.4;
fm = 1955;
Ac = 23.1;
fc = 19550;
fs = 195500;
t  = 0:1/fs:2/fm;
Bf = 4.9;
Bp = 4.9;

em = Am*cos(2*%pi*fm*t);
subplot(4,1,1);
plot(t,em);

ec = Ac*cos(2*%pi*fc*t);
subplot(4,1,2);
plot(t,ec);


efm = Ac*cos(2*%pi*fc*t + Bf*sin(2*%pi*fm*t));
subplot(4,1,3);
plot(t,efm);

epm = Ac*cos(2*%pi*fc*t + Bp*cos(2*%pi*fm*t));
subplot(4,1,4);
plot(t,epm);


```


## Output Waveform:
<img width="1919" height="1197" alt="Screenshot 2026-05-22 135320" src="https://github.com/user-attachments/assets/93b7ce69-bbf0-4a50-9435-ea791b314003" />

<img width="1280" height="720" alt="WhatsApp Image 2026-05-28 at 8 26 36 PM" src="https://github.com/user-attachments/assets/cddc671d-2d91-439e-a0a6-b064a1c59db5" />



## RESULT:
Thus the frequency modulation and demodulation is successfully done and the output is experimentally verified.
