# Algorithm for QR Decomposition
## Aim:
To implement QR decomposition algorithm using the Gram-Schmidt method.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Intialize the matrix Q and u
2.	The vector u and e is given by

    ![eqn1](./ex4.jpg)

    ![eqn2](./ex6.jpg)

    ![eqn3](./ex3.jpg)

3.	Obtain the Q matrix   
    ![eqn4](./ex1.jpg)
4.	Construct the upper triangular matrix R
    ![eqn5](./ex2.jpg)



## Program:
### Gram-Schmidt Method
```

Program to QR decomposition using the Gram-Schmidt method
Developed by: venkatesh A
RegisterNumber: 2122250340485

import os
os.environ["OPENBLAS_NUM_THREADS"] = "1"
import numpy as np
A = np.array(eval(input()))
Q , R = np.linalg.qr(A)
d = np.diag(R)
sign = np.sign(d)
sign[sign == 0] = 1
Q = Q*sign
R = sign[:,np.newaxis] * R
Q[np.isclose(Q,0)] = 0
R[np.isclose(R,0)] = 0
print("The Q Matrix is")
print("",Q)
print("The R Matrix is")
print("",R)







```

## Output

<img width="1202" height="532" alt="image" src="https://github.com/user-attachments/assets/6cd41888-7dc1-4743-a86e-6809aab52ae6" />



## Result
Thus the QR decomposition algorithm using the Gram-Schmidt process is written and verified the result.
