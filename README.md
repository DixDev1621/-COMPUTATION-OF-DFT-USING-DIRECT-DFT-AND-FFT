
# EXP 2 : COMPUTATION OF DFT USING DIRECT DFT AND FFT

# AIM: 

To obtain DFT and FFT of a given sequence in SCILAB. 


# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
# DISCRETE FOURIER TRANSFORM 
```
clc;
clear;
xn=[1 2 3 1 1 2 0 0];
n1=0:1:length(xn)-1;
subplot(3,1,1);
plot2d3(n1,xn);
xlabel('Time n');
ylabel('Amplitude xn');
title('Input Sequence');
j=sqrt(-1);
N=length(xn);
Xk=zeros(1,N);
      for k=0:N-1
          for n=0:N-1
              Xk(k+1)=Xk(k+1)+xn(n+1)*exp((-j*2*%pi*k*n)/N);
      end
end
disp(Xk)
K1=0:1:length(Xk)-1;
magnitude=abs(Xk)
subplot(3,1,2);
plot2d3(K1,magnitude);
xlabel('frequency(Hz)');
ylabel('magnitude(gain)');
title('magnitude spectrum');
angle=atan(imag(Xk),real(Xk))
subplot(3,1,3);
plot2d3(K1,angle);
xlabel('frequency(Hz)');
ylabel('phase');
title('Phase spectrum');
```
# Fast Fourier Transform
```
clc;
clear;
close;
xn=[1 2 3 1 1 2 0 0];
n1=0:1:length(xn)-1;
subplot(2,2,1);
plot2d3(n1,xn);
xlabel('time n');
ylabel('amplitude');
title('input sequence');
xk=fft(xn);
k1=0:1:length(xk)-1;
magnitude=abs(xk)
subplot(2,2,2);
plot2d3(k1,magnitude);
xlabel('frequency(Hz)');
ylabel('magnitude(gain)');
title('magnitude spectrum');

angle=atan(imag(xk),real(xk));
subplot(2,2,3);
plot2d3(k1,angle);
xlabel('frequency(Hz)');
ylabel('Phase');
title('phase spectrum');
y=ifft(xk);
n2=0:1:length(y)-1;
subplot(2,2,4);
plot2d3(n2,y);
xlabel('time n');
ylabel('amplitude');
title('inverse FFT of x(k)');
```

# CALCULATIONS: 

<img width="1025" height="1600" alt="image" src="https://github.com/user-attachments/assets/ec3bdfcc-d2d0-4935-8d01-e02aac33c85a" />

<img width="907" height="1600" alt="image" src="https://github.com/user-attachments/assets/3d7df709-18af-465a-9ff4-b0dc4ed3c835" />

<img width="1197" height="1600" alt="image" src="https://github.com/user-attachments/assets/c6f19ff3-ef5b-47ee-b63d-f9ce1d634ba7" />


# SAMPLE OUTPUT: 
# DISCRETE FOURIER TRANSFORM 
<img width="751" height="711" alt="Screenshot 2026-03-11 005344" src="https://github.com/user-attachments/assets/52e94e85-334b-4443-9d69-a1d647371356" />

# Fast Fourier Transform
<img width="756" height="713" alt="Screenshot 2026-03-11 005451" src="https://github.com/user-attachments/assets/7393f5cf-8f1b-4362-bf85-59c06b8ca493" />


# RESULT: 

Thus, the Discrete Fourier Transform (DFT) and Fast Fourier Transform (FFT) of the given input sequence were successfully computed using SCILAB.

