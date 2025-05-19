#  Mean and variance of a discrete  distribution
~~~
NAME: SRINIVASAN S
REG NO: 212224220105
~~~


# Aim : 

To find mean and variance of arrival of objects from the feeder using probability distribution


# Software required :  

Python and Visual components tool

# Theory:

The expectation or the mean of a discrete random variable is a weighted average of all possible
values of the random variable. The weights are the probabilities associated with the corresponding values. 
It is calculated as,

![image](https://github.com/user-attachments/assets/e28c7f92-eced-45f4-a2fa-7c1a2a50a7c2)

The variance of a random variable shows the variability or the scatterings of the random variables.
It shows the distance of a random variable from its mean. It is calcualted as

![image](https://github.com/user-attachments/assets/83ba466d-fab2-4cfc-abfa-036cb2b722ac)


# Procedure :

1. Construct frequency distribution for the data

2. Find the  probability distribution from frequency distribution.

3. Calculate mean using 

![image](https://github.com/user-attachments/assets/c2004ac9-857d-4913-bc63-b614566a9c23)

4. Find  
   
![image](https://github.com/user-attachments/assets/730d1c90-d26b-4876-9eb8-5eab1129e044)

5.  Calculate variance using 
  

![image](https://github.com/user-attachments/assets/222a430f-2fab-4625-9643-4eb2b2488e7d)


# Experiment :


![image](https://github.com/user-attachments/assets/2a89482d-1d05-4e95-ad83-c5967a6a7e8a)

# Program :

~~~
import numpy as np
L=[int(i) for i in input().split()]
N=len(L); M=max(L) 
x=list();f=list()
for i in range (M+1):
    c = 0
    for j in range(N):
        if L[j]==i:
            c=c+1
    f.append(c)
    x.append(i)
sf=np.sum(f)
p=list()
for i in range(M+1):
    p.append(f[i]/sf) 
mean=np.inner(x,p)
EX2=np.inner(np.square(x),p)
var=EX2-mean**2 
SD=np.sqrt(var)
print("The Mean arrival rate is %.3f "%mean)
print("The Variance of arrival from feeder is %.3f "%var) 
print("The Standard deviation of arrival from feeder is %.3F "%SD)
~~~



# Output : 


![image](https://github.com/user-attachments/assets/3855086e-e8eb-4717-bb28-b22c6001fa58)


# Results :
The mean and variance of arrivals of objects from feeder using probability distribution are calculated.

