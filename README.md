
# SIMULATION-OF-MEAN-AND-VARIANCE-USING-SCILAB

## AIM:
To write a program for mean, variance and cross correlation in SCILAB and verify the output.

## EQUIPMENTS Needed

•	Computer with i3 Processor
•	SCI LAB


## Algorithm
1.	Define	the	Function:	Specify the	function	you	want	to	simulate.	For	example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
2.	Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
3.	Evaluate the Function: Compute the function values at each of these sample points.
4.	Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
5.	Display Results: Output the computed mean variance and Cross Correlation PROCEDURE
•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated results


## PROGRAM
~~~
clear;
clc;
function z = f(x)
z = x * 6 * (1 - x)^2;
endfunction
a = 0;
b = 1;
EX = intg(a, b, f);
function z = c(y)
z = y * 6 * (1 - y)^2;
endfunction
EY = intg(a, b, c);
disp(EX, "i) Mean of X = ");
disp(EY, "Mean of Y = ");
function z = g(x)
z = x^2 * 6 * (1 - x)^2;
endfunction
EX2 = intg(a, b, g);
function z = h(y)
z = y^2 * 6 * (1 - y)^2;
endfunction
EY2 = intg(a, b, h);
vX2 = EX2 - (EX)^2;
vY2 = EY2 - (EY)^2;
disp(vX2, "ii) Variance of X = ");
disp(vY2, "Variance of Y = ");
x = input("Type in the reference sequence = ");
y = input("Type in the second sequence = ");
n1 = max(size(y)) - 1;
n2 = max(size(x)) - 1;
r = corr(x, y, n1);
plot2d3('gnn', r);
xtitle("Cross Correlation");

~~~


## CALCULATION
<img width="1189" height="1599" alt="image" src="https://github.com/user-attachments/assets/42d1f21a-d4b1-4dcc-90bf-db7ee04beb32" />
<img width="969" height="1600" alt="image" src="https://github.com/user-attachments/assets/b1892d24-10fc-4a3b-ba70-ac01e4be05d8" />
<img width="1049" height="1600" alt="image" src="https://github.com/user-attachments/assets/adc69413-9b24-4da0-9493-1d85b5c0ec25" />


## OUTPUT
<img width="1919" height="1079" alt="Screenshot 2026-05-24 190607" src="https://github.com/user-attachments/assets/5bbc64df-bf4d-4bbb-a1bd-c78358bb5afe" />

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/1ba5fb24-8046-4bfb-98b1-42142b489ec2" />



## RESULT:
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.
