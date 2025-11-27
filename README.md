# Radar-Range-Equation

### Aim:

To calculate the maximum range of a radar system using the Radar Range equation and verify through Python Programming.

---

### Theory:

The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum range at which a radar can detect a target. It is given by:

$$R_{max} = \left(\frac{P_t G \sigma A_e}{(4 \pi)^2 S_{min}} \right)^{\frac{1}{4}}$$

---

### Procedure:

1. Set Up the Python Enviroment:Ensure that Pytho is installed on your system. You can use Anaconda for managing Python packages and environments, or any other Python IDE of your choice.
2. Import Necessary Libraries: Import the math library in Python.
3. Define the Radar Range Equation Function: Create a function to calculate the maximum range using the Radar Range Equation.
4. Input Parameters for the Radar System: Define the input parameters such as transmitted power, transmitter gain, receiver gain, radar frequency, radar cross section and minimum detectable power.
5. Calculate the Maximum Range: Use the function to calculate the maximum range of the radar.
6. Execute the program: Run the Python script to calculate and display the maximum range of the radar.

---

### Program:

```sci
clc;
clear;
c = 3e8; 

Gt = 25;
Gr = 25;
f = 10e9; 
sigma = 1; 
Pmin = 1e-10;
lambda = c / f;
Pt = [100, 500, 1000, 2000, 5000, 10000];
Rmax = zeros(Pt);
for i = 1:length(Pt)
    Rmax(i) = ((Pt(i) * Gt * Gr * (lambda^2) * sigma) / ((4 * %pi)^3 * Pmin))^(1/4);
end

scf(0);
plot(Pt, Pt, 'r', 'LineWidth', 2);

scf(1);
plot(Pt, Rmax, 'b', 'LineWidth', 2);

scf(2);
plot(Rmax, Pt, 'g', 'LineWidth', 2);

disp("Transmitted Power (W)   |   Maximum Range (m)");
disp([Pt' Rmax']);

```

---

### Output Waveform:

<img width="1919" height="1134" alt="image" src="https://github.com/user-attachments/assets/e455ff15-1211-41e6-be48-acc25cb427af" />

---

### Manual Calculation:

![WhatsApp Image 2025-11-27 at 19 26 28_bd4ada28](https://github.com/user-attachments/assets/d70ed385-dfa4-46f1-9ce8-da42b5e6515e)

---

### Result:

Thus, the value of maximum range of a radar of a radar system calculated using the Radar Equation is successfully verified using Scilab programming.
