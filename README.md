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
wc1=input('enter the value of cut off frequency wc1'); 
wc2=input('enter the value of cut off frequency wc2'); 
N=input('enter the value of filter'); 
alpha=(N-1)/2; 
eps=0.001; 
%Band Pass Filter Coefficient
n=0:1:N-1; 
hd=(sin(wc1*(n-alpha+eps))-sin(wc2*(n-alpha+eps)))./((n-alpha+eps)*pi)
%Bartlett Window Sequence 
n=0:1:N-1; 
wh = 1 - abs(n - alpha) / alpha;
hn=hd.*wh
% Plot the Band Pass Filter with Hanning Window Technique
w=0:0.01:pi; 
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');
```

## OUTPUT:
<img width="802" height="734" alt="Screenshot 2025-11-17 175508" src="https://github.com/user-attachments/assets/b5b724a6-4455-448e-bd5a-ce1b02dc24df" />

## RESULT:
![6](https://github.com/user-attachments/assets/ca39a474-e7b8-46be-bf89-a9a16272251a)

