***Heaven’s Light is Our Guide***

**Rajshahi University of Engineering & Technology**

![](Aspose.Words.d6618a9b-d629-4045-9499-7a1877110931.001.jpeg)

`      `**Department of Electrical & Computer Engineering**



**Course No: ECE 4124**

**Course Title: Digital Signal Processing Sessional**

**Experiment Date:22/05/23**

**Submission Date: 08/06/23**







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














**Experiment No: 05** 

**Experiment Name:**  Study of Z Transform of Causal, Non-causal and Anti-causal Signal.


**Theory:**

The Z-transform is a powerful tool in digital signal processing that allows us to analyze discrete-time signals and systems. It is an extension of the discrete Fourier transform (DFT) and provides a representation of a discrete-time signal or system in the complex domain.

The Z-transform of a causal signal is defined for sequences that are non-zero only for non-negative time indices. In other words, a causal signal is one that starts at or after time index zero. The Z-transform of a causal signal X[n] is given by:

X(z) = ∑(n=0 to ∞) x[n] \* z^(-n)

Here, x[n] represents the samples of the causal signal, and z is a complex variable. The Z-transform provides a representation of the signal in terms of z, which can be analyzed to understand its properties and behavior.

On the other hand, the Z-transform of a non-causal signal is defined for sequences that are non-zero for negative as well as non-negative time indices. In other words, a non-causal signal has values before time index zero. The Z-transform of a non-causal signal X[n] is given by:

X(z) = ∑(n=-∞ to ∞) x[n] \* z^(-n)

In this case, the summation is performed over the entire range of n, including negative time indices.

**Used Tools: MATLAB**







**Code for Causal:**				

clear all					

close all

clc

x=[**3** **1** **2** **4**]

l=length(x)

z=sym('z')

X=**0**

p=l

**for** i=**0**:l-**1**

`    `X=X+x(p)\*z^(i)

`    `%p=p-**1**

end

display(X)

**Output:**						 

![](Aspose.Words.d6618a9b-d629-4045-9499-7a1877110931.004.png)								

















**Code for Anti-causal:**

clear all

close all

clc

x=[**3** **1** **2** **4**]

l=length(x)

z=sym('z')

X=**0**

**for** i=**0**:l-**1**

`    `X=X+x(i+**1**)\*z^(-i)



end

%p=roots(x)

display(x)



**Output:**

![](Aspose.Words.d6618a9b-d629-4045-9499-7a1877110931.006.png)














**Code for Non-causal:**

clear all;

close all;

clc;

syms z n

x = [2 3 5 6 8 9];

zero=3;

len=length(x);



X=0;

z=sym('z');



for i=0:zero-1

`    `X=X+x(i+1).\*z^(i);

end

for i=zero:len-1

`    `X=X+x(i+1).\*z^(-i);

end

disp(X);

Output:

![](Aspose.Words.d6618a9b-d629-4045-9499-7a1877110931.007.png)


**Discussion & Conclusion:**

In this experiment the z transform of  causal, anti-causal and non-causal signal was done basically. The first two that means causal and anti-causal signals output was got without any error but for the z transform of non-causal signals, there created some logic error, such as in the for loop condition wasn’t fulfilled in the primary level. For some position, the value wasn’t found. But later the problem was solved. And all the z transform can be noticed from the output figure. 



