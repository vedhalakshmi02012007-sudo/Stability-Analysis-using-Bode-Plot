# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:

![WhatsApp Image 2025-11-05 at 08 58 33_74c946e1](https://github.com/user-attachments/assets/873f462c-6129-4869-a96c-18fe14218c52)
![WhatsApp Image 2025-11-05 at 08 58 47_9f1d8d4e](https://github.com/user-attachments/assets/5888c494-5dc7-4e78-b89b-32755fc7620c)
![WhatsApp Image 2025-11-05 at 08 59 00_3e5a93d1](https://github.com/user-attachments/assets/718caf74-9a8d-40f3-be71-79d2952f9866)
![WhatsApp Image 2025-11-05 at 08 59 06_306d1cfa](https://github.com/user-attachments/assets/1f89a678-9acc-4add-b36d-9e370cdc6932)




## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
num=[1];
den=[0.05 0.6 1 0];
sys=tf(num,den)
bode(sys)
grid on;
[gm pm wpc wgc]=margin(sys)
gmindb=20*log10(gm)
if(wpc>wgc)
    disp('stable')
elseif(wpc==wgc)
    disp('marginally stable')
else
    disp('unstable')
end
```
## Output:

<img width="1711" height="1007" alt="image" src="https://github.com/user-attachments/assets/d925d36b-6707-4801-b689-6e57d54714e9" />

## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB.<br>
Gain margin = 12<br>
Phase Margin = 60<br>
Gain crossover frequency = 0.907<br>
Phase crossover frequency = 4.4721<br>
The system is stable.<br>
