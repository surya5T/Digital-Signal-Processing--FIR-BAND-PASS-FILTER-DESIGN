# Digital-Signal-Processing--FIR-BAND-PASS-FILTER-DESIGN
## AIM:
To generate design of Band Pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Band Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
```
clc; % clear screen
clear all; % clear screen
close all; % close all figure windows
wc=input('enter the value of cut off frequency');
N=input('enter the value of filter');
alpha=(N-1)/2;
eps=0.001;
%High Pass Filter Coefficient
n=0:1:N-1;
hd=(sin(pi*(n-alpha+eps))-sin((n-alpha+eps)*wc))./(pi*(n-alpha+eps))
%Hamming Window Sequence
n=0:1:N-1;
wh=0.54-0.46*cos((2*pi*n)/(N-1))
hn=hd.*wh
% Plot the High Pass Filter with Hamming Window Technique
w=0:0.01:pi;
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');

```
## OUTPUT:
![b3405e1f-f685-4318-ba6b-e9e2f5edc34e](https://github.com/user-attachments/assets/f2214bb2-59b3-4be5-80eb-53b8a315c9bb)

## RESULT:
![d4524dd8-6e1c-4ed2-a3ba-583bd30ee2d7](https://github.com/user-attachments/assets/bf17997d-ac3e-407a-b765-bfcfd3fc3d8c)
