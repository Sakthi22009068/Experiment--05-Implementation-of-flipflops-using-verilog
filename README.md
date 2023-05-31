# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
/* write all the steps invloved */
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: 
RegisterNumber:  


### PROGRAM SR
```
module srflipflop(s,r,clk,q,qbar);
input s,r,clk;
output q,qbar;
reg q,qbar;
always @(posedge clk)
begin 
q<=s|(~r&q);
qbar<=r|(~s&~q);
end
endmodule
```






### RTL LOGIC FOR FLIPFLOPS 

![rtl srf (2)](https://github.com/Sakthi22009068/Experiment--05-Implementation-of-flipflops-using-verilog/assets/130567548/3d2955a8-aa31-4788-91e3-46eb0001904f)








### TIMING DIGRAMS FOR FLIP FLOPS 
![td srf (2)](https://github.com/Sakthi22009068/Experiment--05-Implementation-of-flipflops-using-verilog/assets/130567548/75d773dd-d31c-4b2c-b512-f420192a62f9)


### PROGRAM JK
```
module jkflipflop(j,k,clk,q,qbar);
input j,k,clk;
output q,qbar;
reg q,qbar;
always @(posedge clk)
begin 
q<=(j&~q)|(~k&q);
qbar<=~q;
end
endmodule
```






### RTL LOGIC FOR FLIPFLOPS 

![rtl jkf](https://github.com/Sakthi22009068/Experiment--05-Implementation-of-flipflops-using-verilog/assets/130567548/15af1a3d-7c95-4fb0-98ae-d2da23635d9e)








### TIMING DIGRAMS FOR FLIP FLOPS 
![td jkff](https://github.com/Sakthi22009068/Experiment--05-Implementation-of-flipflops-using-verilog/assets/130567548/0af4c6e9-82fb-4b08-96f1-60f478d8c278)


### PROGRAM T
```
module tflipflop(clk,t,q,qbar);
input clk,t;
output q,qbar;
reg q,qbar;
always @(posedge clk)
begin
q<=(t&~q)|(~t&q);
qbar<=~q;
end 
endmodule
```






### RTL LOGIC FOR FLIPFLOPS 

![rtl tff](https://github.com/Sakthi22009068/Experiment--05-Implementation-of-flipflops-using-verilog/assets/130567548/2c2714de-5bea-46fd-a165-12b99815c286)








### TIMING DIGRAMS FOR FLIP FLOPS 
![td tff](https://github.com/Sakthi22009068/Experiment--05-Implementation-of-flipflops-using-verilog/assets/130567548/ea94caf4-d299-4b85-8e4a-79d7b941c446)


### PROGRAM D
```
module dflipflop(d,clk,q,qbar);
input d,clk;
output q,qbar;
reg q,qbar;
always @(posedge clk)
begin
q<=d;
qbar<=~q;
end
endmodule
```






### RTL LOGIC FOR FLIPFLOPS 
![rtl dff](https://github.com/Sakthi22009068/Experiment--05-Implementation-of-flipflops-using-verilog/assets/130567548/19186638-48a0-47fc-b7f2-635bc3675c8d)









### TIMING DIGRAMS FOR FLIP FLOPS 

![td dff](https://github.com/Sakthi22009068/Experiment--05-Implementation-of-flipflops-using-verilog/assets/130567548/68ccd884-28de-4774-b0ca-e010156c2ef1)







### RESULTS 
All the flip flops are implemented using verilog and their functionality has been validated using their functional tables.
