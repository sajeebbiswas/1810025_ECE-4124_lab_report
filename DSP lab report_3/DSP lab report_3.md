***Heaven’s Light is Our Guide***

**Rajshahi University of Engineering & Technology**

![](Aspose.Words.8c1bdb24-9b32-4f82-a930-ac7b4f948555.001.jpeg)

`      `**Department of Electrical & Computer Engineering**



**Course No: ECE 4124**

**Course Title: Digital Signal Processing Sessional**

**Experiment Date:08/05/23**

**Submission Date: 15/05/23**







**Submitted To**,

Hafsa Binte Kibria

Lecturer, 

Department of Electrical & Computer Engineering (ECE)

RUET


**Submitted By**,

Sajeeb Biswas

ID: 1810025

Department of Electrical & Computer Engineering (ECE)

RUET














**Experiment No: 03**

**Experiment Name:**  Study of Auto Correlation and Cross Correlation with and                          without Using Built in function.


**Theory:**

In digital signal processing (DSP), autocorrelation is a technique used to measure the similarity or correlation of a signal with itself at different time delays. It is commonly used in fields such as audio processing, speech recognition, and image processing.

The autocorrelation of a discrete-time signal x[n] is defined by the following equation:

Rxx[k] = sum(x[n] \* x[n-k])

Where:

- Rxx[k] represents the autocorrelation at lag k.
- x[n] is the input signal at time index n.
- k is the lag, indicating the time delay between two instances of the signal.

The autocorrelation function calculates the similarity between the original signal and a shifted version of itself at different time lags. It is often used to identify periodic or repetitive patterns within a signal, as the autocorrelation will exhibit peaks at the corresponding lag values.

Cross-correlation is a technique used in digital signal processing (DSP) to measure the similarity or correlation between two signals. It is commonly employed in fields such as audio processing, image registration, and communication systems.

The cross-correlation of two discrete-time signals x[n] and y[n] is defined by the following equation:

Rxy[k] = sum(x[n] \* y[n-k])

Where:

- Rxy[k] represents the cross-correlation at lag k.
- x[n] is the first input signal at time index n.
- y[n] is the second input signal at time index n.
- k is the lag, indicating the time delay between the two signals.

The cross-correlation function calculates the similarity between the two signals at different time lags. It is often used to determine the time delay or phase shift between signals, detect signal echoes or echoes, align signals in synchronization, and analyze the similarity between two signals.



**Used Tools: Matlab**

**Code:**

`				`**Auto Correlation**

With built in function:				

|||
| :- | :- |

|<p>` `1</p><p>` `2</p><p>` `3</p><p>` `4</p><p>` `5</p><p>` `6</p><p>` `7</p><p>` `8</p><p>` `9</p><p>10</p><p>11</p><p>12</p><p>13</p><p>14</p><p>15</p><p>16</p>|<p>clear all;</p><p>close all;</p><p>clc;</p><p>x=input('Enter the input sequence:');</p><p>c=xcorr(x,x);</p><p>axis tight</p><p>**subplot**(**2**,**1**,**1**);</p><p>stem(x);</p><p>xlabel('time');</p><p>ylabel('amplitude');</p><p>title('Input signal');</p><p>subplot(**2**,**1**,**2**);</p><p>stem(c);</p><p>xlabel('time');</p><p>ylabel('amplitude');</p><p>title('Auto correlation');</p>|
| :- | :- |





























Without built in function:


clc;

clear all;

x= input('Enter a sequence');

y= fliplr(x);

L= length(x);

M= length(y);

N= L+M-**1**;

x=[x, zeros(**1**,N-L)];

y=[y, zeros(**1**,N-M)];

h=zeros(N,N);

%k=**0**;

**for** j=**1**:N

`    `**for** k=**0**:N-**1**

`        `**if**(j+k<=N)

`            `h(j+k,j)=x(k+**1**);

`        `**else**

`            `**h**(j+k-N,j)=x(k+**1**);

`        `end

`    `end

end

c=(h\*y')';

axis tight

**subplot**(**2**,**1**,**1**);

stem(x);

xlabel('time');

ylabel('amplitude');

title('Input signal');

subplot(**2**,**1**,**2**);

stem(c);

xlabel('time');

ylabel('amplitude');

title('Auto correlation2');




































**Output:**

![](Aspose.Words.8c1bdb24-9b32-4f82-a930-ac7b4f948555.006.png)

![](Aspose.Words.8c1bdb24-9b32-4f82-a930-ac7b4f948555.007.png)

Figure 3.1: Input and Output Signal for Auto Correlation




`					`**Cross Correlation**

Without built in function:

clc;

clear all;

x= input('Enter **1**st input sequence');

h= input('Enter **2**nd input sequence');

y= fliplr(h);

L= length(x);

M= length(y);

N= L+M-**1**;

x=[x, zeros(**1**,N-L)];

y=[y, zeros(**1**,N-M)];

z=x;

h=zeros(N,N);

k=**0**;

**for** j=**1**:N

`    `**for** k=**0**:N-**1**

`        `**if**(j+k<=N)

`            `h(j+k,j)=x(k+**1**);

`        `**else**

`            `**h**(j+k-N,j)=x(k+**1**);

`        `end

`    `end

end

c=(h\*y')';

axis tight

**subplot**(**3**,**1**,**1**);

stem(x);

xlabel('time');

ylabel('amplitude');

title('**1**st Input signal');

subplot(**3**,**1**,**2**);

stem(c);

xlabel('time');

ylabel('amplitude');

title('**2**nd Input signal');

subplot(**3**,**1**,**2**);

stem(c);

xlabel('time');

ylabel('amplitude');

title('Cross correlation');
























Output:

![](Aspose.Words.8c1bdb24-9b32-4f82-a930-ac7b4f948555.010.png)

![](Aspose.Words.8c1bdb24-9b32-4f82-a930-ac7b4f948555.011.png)

Figure 3.2: Input and Output Signal for Cross Correlation






**Discussion & Conclusion:**

Here we have spoken about the fundamental ideas behind auto and cross correlation as well as how they are used in signal processing. Additionally, we have given MATLAB computation examples for auto- and cross-correlation. All the sample input that was taken here are provided right answer and it also matches the theory. The output curve also plotted in this report and from there we can observe the correct sequence. 

Overall, auto and cross correlation are effective methods for processing and evaluating data, and many engineering and scientific disciplines use them.





References:

[1] <https://www.allaboutcircuits.com/technical-articles/understanding-correlation/>
