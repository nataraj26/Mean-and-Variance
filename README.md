#  Mean and variance of a discrete  distribution


# Aim : 

To find mean and variance of arrival of objects from the feeder using probability distribution


# Software required :  

Python and Visual components tool

# Theory:

The expectation or the mean of a discrete random variable is a weighted average of all possible
values of the random variable. The weights are the probabilities associated with the corresponding values. 
It is calculated as,
![image](https://github.com/user-attachments/assets/ba623ce5-f708-4a8b-adbc-fc073f47f66a)


The variance of a random variable shows the variability or the scatterings of the random variables.
It shows the distance of a random variable from its mean. It is calcualted as

![image](https://github.com/user-attachments/assets/ee7696e7-a4e1-410f-945a-158ac700eb6e)



# Procedure :

1. Construct frequency distribution for the data

2. Find the  probability distribution from frequency distribution.

3. Calculate mean using 
![image](https://github.com/user-attachments/assets/32d1a09e-6d22-4853-bdf1-fa2d1da0c99b)
   
  
4. Find  
   ![image](https://github.com/user-attachments/assets/50b466f1-4dba-4cc9-a548-2f5272a38232)

     

5.  Calculate variance using 
  
 ![image](https://github.com/user-attachments/assets/054f381d-4997-41fa-b43c-3ae5b72fc155)
 


# Experiment :

![image](https://github.com/user-attachments/assets/afa113c6-eb6f-4697-b448-f25b80dc34f1)

# Program :
```
Name : Nataraj kumaran S
Reg No :212223230137
```
```
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
```

# Output : 
![386151568-41c3c042-fb12-43a7-b9ab-a8b188ac39b4](https://github.com/user-attachments/assets/91b33c1b-35e0-4079-8aad-5fe8f2894966)


# Results :
The mean and variance of arrivals of objects from feeder using probability distribution are calculated.

