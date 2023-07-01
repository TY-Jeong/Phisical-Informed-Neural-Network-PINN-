# pinn_damped-harmonic-oscillator
>>This project addressed inverse problem of PINN (Physical Informed Neural Network) with nosiy data.

This neural network predicts the exact ODE equation and the corresponding solution for damped harmonic oscillator. In contrast to common PINNs, I considered data including random noise which makes far harder to predict the exact ODE.  
To alleviate the nosie effect, the loss responsible to ODE was weighted using a sigmoid function. Hence, my network concentrates the noisy data to get a crued solution in early training steps, while the influence of the ODE is emphasized in later steps (In other words, the influence of the noisy data will be getting lower). This network can effectively search the exact solution and the ODE.

For forward problem of PINN, See https://github.com/johninkorea/CAC23_parallel_computing/tree/main  
For description of damped harmonic oscillator, See https://beltoforion.de/en/harmonic_oscillator/

![](./results/pinn_ver5.gif)

