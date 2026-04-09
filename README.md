# EVALUATION-OF-RADAR-RANGE
Aim:
To calculate the maximum range of a radar system using the Radar Range Equation and verify the results through SCILAB

Theory:
The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum range at which a radar can detect a target. It is given by:


<img width="552" height="453" alt="image" src="https://github.com/user-attachments/assets/9efc82cf-a3d8-4113-8f55-cbaea4307353" />

---
Procedure:


Set Up the SCILAB Environment: Ensure that SCILAB is installed on your system.
Define the Radar Range Equation Function: Create a function to calculate the maximum range using the Radar Range Equation.
Input Parameters for the Radar System: Define the input parameters such as transmitted power, transmitter gain, receiver gain, radar frequency, radar cross section, and minimum detectable power.
Calculate the Maximum Range: Use the function to calculate the maximum range of the radar.
Execute the Program: Run the Python script to calculate and display the maximum range of the radar.

---
Program:
```
Gt = 48;

Gr = 48;

lambda = 0.08;

sigma = 2;

Pmin = 1e-10;

Pt = linspace(1,1000,100);

Rmax1 = ((Pt .* Gt .* Gr .* lambda^2 .* sigma) ./ ((4*%pi)^3 .* Pmin)).^(1/4);

subplot(2,1,1)

plot(Pt, Rmax1)

Pt_const = 700;

Pmin2 = linspace(1e-12,1e-8,100);

Rmax2 = ((Pt_const .* Gt .* Gr .* lambda^2 .* sigma) ./ ((4*%pi)^3 .* Pmin2)).^(1/4);

subplot(2,1,2)

plot(Pmin2, Rmax2)
```
Calculation:
![WhatsApp Image 2026-04-09 at 08 46 54](https://github.com/user-attachments/assets/1fea75ea-34cd-4d7b-b860-527fa2dc4ad2)

---

Result:

Thus, the maximum range of a radar system using the Radar Range Equation is verified through a Python program.

