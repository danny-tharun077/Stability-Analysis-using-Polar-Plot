# Stability-Analysis-using-Polar-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=10/(S(1+0.5S)(1+0.2S)) using polar plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
![WhatsApp Image 2025-11-17 at 18 03 18_2010bf9c](https://github.com/user-attachments/assets/fea70dc3-993a-413e-a2b8-cbdf5760c452)

![WhatsApp Image 2025-11-17 at 18 03 18_439a4a75](https://github.com/user-attachments/assets/76926eeb-9ba2-46c6-8026-56a8d60fadf1)


## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
~~~
num=[10]
den=[0.1 0.7 1 0]
sys=tf(num,den)
[mag,phase,W]=bode(sys)
mag=squeeze(mag)
phase=squeeze(phase)
phase1=deg2rad(phase)
polarplot(phase1,mag,'linewidth',1.5)
grid on
[Gm Pm Wpc Wgc]=margin(sys)
if(Wpc>Wgc)
    disp('stable')
elseif(Wpc == Wgc)
    disp('marginally stable')
else
    disp('unstable')
end
~~~

## Output:

<img width="695" height="523" alt="image" src="https://github.com/user-attachments/assets/aaa12a59-92a1-4e91-96ef-61c7cc597777" />



## Result:
Thus the polar plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 0.70

Phase Margin = -8.88

Gain crossover frequency = 3.75

Phase crossover frequency = 3.16

The system is  UNSTABLE
