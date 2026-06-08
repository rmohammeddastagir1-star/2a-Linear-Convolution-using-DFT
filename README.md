EXPT 2a: LINEAR CONVOLUTION-USING-DFT
AIM
To perform and verify linear convolution operation of two given sequences using SCILAB.

APPARATUS REQUIRED
PC installed with SCILAB

PROGRAM:
LINEAR CONVOLUTION
```asm
clc;
clear;
x = [10 10 10 10];
h = [2 4 6 8];
m = length(x);
n = length(h);
a = 0:m-1;
b = 0:n-1;
subplot(3,1,1);
plot2d3(a, x);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Input Signal X');
subplot(3,1,2);
plot2d3(b, h);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Impulse Signal h');
y = zeros(1, m+n-1);
for i = 1:(m+n-1)
conv_sum = 0;
for j = 1:i
if ((j <= m) & ((i-j+1) <= n))
conv_sum = conv_sum + x(j) * h(i-j+1);
end
end
y(i) = conv_sum;
end
disp(y, 'Convolution Sum using Direct Formula Method = ');
subplot(3,1,3);
t = 0:(m+n-2);
plot2d3(t, y);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Output Signal y');

```





### CALCULATIONS:
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/227019c2-8ea3-4b56-ad30-1d0129fe9909" />
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/4ff3a2f6-2d94-4e90-8608-b5ee1b376a72" />
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/f197e46a-eecf-4c71-8084-640a6a910799" />




### SAMPLE OUTPUT:
<img width="1365" height="1600" alt="image" src="https://github.com/user-attachments/assets/67a77b68-f638-40cb-a276-fae877d0d69d" />





RESULT:
Thus, the linear convolution of the two given sequences were performed and its result was verified.
