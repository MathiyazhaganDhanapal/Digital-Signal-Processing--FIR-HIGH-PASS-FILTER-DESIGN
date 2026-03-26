# Digital-Signal-Processing--FIR-HIGH-PASS-FILTER-DESIGN
## AIM:
To generate design of High pass FIR digital filter using Blackman Window.
## Software Required:
MAT LAB R2023a.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the hIGH Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
~~~

clc; % clear screen 
clear all; % clear screen 
close all; % close all figure windows 
wc=input('enter the value of wc=');  
N=input('enter the value of N='); 
alpha=(N-1)/2;  
eps=0.001;  
%High Pass Filter Coefficient 
n=0:1:N-1;   
hd=(sin(pi*(n-alpha+eps))-sin((n-alpha+eps)*wc))./(pi*(n-alpha+eps)) 
%Blackman Window Sequence  
n=0:1:N-1;  
wh=0.42-0.5*cos((2*pi*n)/(N-1))+0.08*cos((4*pi*n)/(N-1)) 
hn=hd.*wh  
% Plot the Band Pass Filter with Blackman Window Technique 
w=0:0.01:pi;  
h=freqz(hn,1,w); 
plot(w/pi,abs(h),'blue');

~~~
## OUTPUT:

<img width="1592" height="864" alt="image" src="https://github.com/user-attachments/assets/1ce43d5a-7be7-4d43-801f-f2dd887b2ccd" />

## OUTPUT CALCULATION:

<img width="1865" height="763" alt="image" src="https://github.com/user-attachments/assets/88c5e32f-98bb-4c70-84cb-e2fc288d0490" />


## RESULT:

Thus the design of High pass FIR digital filter using Blackman waveforms were plotted 
and output was verified. 
