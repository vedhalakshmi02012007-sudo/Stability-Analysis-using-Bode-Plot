# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:

![WhatsApp Image 2025-11-16 at 14 10 59_2e0f8893](https://github.com/user-attachments/assets/7d1f21c0-8114-41ab-8ad1-4439cb658694)

![WhatsApp Image 2025-11-16 at 14 10 59_217c8ece](https://github.com/user-attachments/assets/2b2e017e-76ff-4824-b200-0f5b7361b37e)

<img width="1080" height="1421" alt="image" src="https://github.com/user-attachments/assets/5775c85d-9937-41a3-9beb-c11e97dd8120" />

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
