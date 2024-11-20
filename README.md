# DSP-EXP-7A
clc;
clear all;
close all;
N=input('Enter the sequence length N:');
M=input('Enter the down sampling factor M:');
f1=0.05;
f2=0.2;
t=0:1:N-1;
x=sin(2*pi*f1*t)+sin(2*pi*f2*t);
x1=x(1:M:N);
t1=1:1:N/M;
subplot(3,1,1);
plot(t,x);
xlabel('time-->');
ylabel('amplitude-->');
title('Input analog signal');
subplot(3,1,2);
stem(t,x);
xlabel('n-->');
ylabel('amplitude-->');
title('Sampled signal');
subplot(3,1,3);
stem(t1-1,x1);
xlabel('n-->');
ylabel('amplitude==>');
title('Down sampled signal')
