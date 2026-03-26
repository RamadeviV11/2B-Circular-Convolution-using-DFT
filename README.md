# EXPT 2B:CIRCULAR-CONVOLUTION-USING-DFT
## AIM
To perform and verify circular convolution operation of two given sequences using SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM:
```
clc; clear; 
x=[1 1 1 1]; 
n1=0:1:length(x)-1; 
subplot(3,1,1); 
plot2d3(n1,x); 
xlabel('time'); 
ylabel('amplitude'); 
title('input sequence'); 
h=[1 2 3]; 
n2=0:1:length(h)-1; 
subplot(3,1,2); 
plot2d3(n2,h); 
xlabel('time'); 
ylabel('amplitude'); 
title('impulse sequence'); 
N1=length(x); 
N2=length(h); 
N=max(N1,N2); 
N3=N1-N2; 
if(N3>0) 
h=[h,zeros(1,N3)]; 
else 
x=[x,zeros(1,abs(N3))]; 
end 
disp(x) 
disp(h) 
for n=1:N 
y(n)=0; 
for i=1:N 
j=n-i+1; 
if(j<=0) 
end 
j=N+j; 
y(n)=y(n)+x(i)*h(j); 
end 
end 
disp(y) 
n=0:N-1; 
subplot(3,1,3); 
plot2d3(n,y); 
xlabel('time'); 
ylabel('amplitude'); 
title('circular convolution');
```
## CIRCULAR CONVOLUTION

### CALCULATIONS:

![WhatsApp Image 2026-03-26 at 6 38 21 PM (1)](https://github.com/user-attachments/assets/e45218e9-c85f-4b8a-9861-8ec15d947b8a)

### OUTPUT:

![WhatsApp Image 2026-03-26 at 6 41 42 PM (1)](https://github.com/user-attachments/assets/3e439e7f-f99f-44c2-9d37-7d85ed90f67e)


## RESULT:
Thus, the circular convolution of the two given sequences were performed and its result was verified.

