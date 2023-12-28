Developed by: SRIKARAN M<br>
Refrence number:23010618

# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://github.com/Srikaran077/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151993143/52a8f111-f217-42a1-8d13-e5679ad90bbb)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.

![image](https://github.com/Srikaran077/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151993143/6453a112-68b1-449f-9149-34d303853c44)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://github.com/Srikaran077/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151993143/890634ff-66a4-43fd-90c2-5629ee389af3)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://github.com/Srikaran077/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151993143/48d797cc-971c-47ed-bc39-9f06368a3bd2)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.

![image](https://github.com/Srikaran077/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151993143/2d2f0d5d-f713-4646-9063-8d159f31b027)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://github.com/Srikaran077/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151993143/a262f068-6142-4c3a-a5cb-a90ae59b4cd9)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.


![image](https://github.com/Srikaran077/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151993143/09e602b4-db26-4acb-bfe8-cc21e941ab1b)

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://github.com/Srikaran077/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151993143/5a0d5d6d-7416-4e32-8e28-c892b11a4410)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://github.com/Srikaran077/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151993143/81f62197-6160-4b07-83ff-0c64e75e3d39)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
![image](https://github.com/Srikaran077/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151993143/1f5085ef-d220-4f32-a764-123cc5339af9)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://github.com/Srikaran077/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151993143/81dd21df-4889-4765-90b6-68d0b274c17b)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://github.com/Srikaran077/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151993143/848a178f-7f86-4b35-a6e3-32dac7877c68)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
1.Using nand gates and wires construct sr flip flop.
2.Repeat same steps to construct JK,D,T flipflops.
3.Find Rtl logic and timing diagram for all flipflops.
4.end the program
### PROGRAM 
SR Flip-Flop:
module SR_flipflop(S,R,clk,Q,Qbar);
input S,R,clk;
output Q,Qbar;
wire X,Y;
nand (X,S,clk);
nand (Y,R,clk);
nand (Q,X,Qbar);
nand (Qbar,Y,Q);
endmodule

D Flip-Flop:
module D_flipflop(D,clk,Q,Qbar);
input D,clk;
output Q,Qbar;
assign Dbar=~D;
wire X,Y;
nand (X,D,clk);
nand (Y,Dbar,clk);
nand (Q,X,Qbar);
nand (Qbar,Y,Q);
endmodule

JK Flip-Flop:
module JK_flipflop(J,K,clk,Q,Qbar);
input J,K,clk;
output Q,Qbar;
wire X,Y;
nand (X,J,clk,Qbar);
nand (Y,K,clk,Q);
nand (Q,X,Qbar);
nand (Qbar,Y,Q);
endmodule

T Flip-Flop:
module T_flipflopo(T,clk,Q,Qbar);
input T,clk;
output Q,Qbar;
wire S,R;
nand (S,T,clk,Qbar);
nand (R,T,clk,Q);
nand (Q,S,Qbar);
nand (Qbar,R,Q);
endmodule

### RTL LOGIC FOR FLIPFLOPS 
SR Flip-Flop:

![image](https://github.com/Srikaran077/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151993143/cc5ba961-8761-4834-b879-70ccf2edb434)

D Flip-Flop:

![image](https://github.com/Srikaran077/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151993143/d2126ec9-68db-40d5-a669-e0dc9a65299d)

JK Flip-Flop:

![image](https://github.com/Srikaran077/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151993143/e1fd7b34-e2c1-4af4-a62d-648dc52cd512)

T Flip-Flop:

![image](https://github.com/Srikaran077/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151993143/e4acf67b-c59a-436b-b75c-a18f13cd1e59)

### TIMING DIGRAMS FOR FLIP FLOPS 
SR Flip-Flop:

![image](https://github.com/Srikaran077/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151993143/6b2bc704-9e38-49d3-9d96-e026acd174ef)

D Flip-Flop:


JK Flip-Flop:

![image](https://github.com/Srikaran077/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151993143/641974ed-f38a-489a-bfa4-0c9ca95b2edd)

T Flip-Flop:

![image](https://github.com/Srikaran077/Experiment--05-Implementation-of-flipflops-using-verilog/assets/151993143/9513fa34-dd55-490b-b54b-ebe612023447)

### RESULTS 
Thus implementation of SR, JK, D and T flipflops using nand gates are done sucessfully.
