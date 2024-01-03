# Experiment-06 Synchornous counters up counter
### AIM: To implement 4 bit up and down counters and validate  functionality.
### Name: RAVIVARMAN G S
### Register number: 23006420
##### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
##### SOFTWARE REQUIRED:   Quartus prime
### THEORY 

## UP COUNTER 
The counter is a digital sequential circuit and here it is a 4 bit counter, which simply means it can count from 0 to 15 and vice versa based upon the direction of counting (up/down). 

The counter (“count“) value will be evaluated at every positive (rising) edge of the clock (“clk“) cycle.
The Counter will be set to Zero when “reset” input is at logic high.
The counter will be loaded with “data” input when the “load” signal is at logic high. Otherwise, it will count up or down.
The counter will count up when the “up_down” signal is logic high, otherwise count down

Since we know that binary count sequences follow a pattern of octave (factor of 2) frequency division, and that J-K flip-flop multivibrators set up for the “toggle” mode are capable of performing this type of frequency division, we can envision a circuit made up of several J-K flip-flops, cascaded to produce four bits of output.
The main problem facing us is to determine how to connect these flip-flops together so that they toggle at the right times to produce the proper binary sequence.
Examine the following binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1:
Binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1.

Note that each bit in this four-bit sequence toggles when the bit before it (the bit having a lesser significance, or place-weight), toggles in a particular direction: from 1 to 0.



 
 

Starting with four J-K flip-flops connected in such a way to always be in the “toggle” mode, we need to determine how to connect the clock inputs in such a way so that each succeeding bit toggles when the bit before it transitions from 1 to 0.

The Q outputs of each flip-flop will serve as the respective binary bits of the final, four-bit count:

 

Four-bit “Up” Counter
![image](https://user-images.githubusercontent.com/36288975/169644758-b2f4339d-9532-40c5-af40-8f4f8c942e2c.png)



### Procedure
1. Create a New Project:
   - Open Quartus and create a new project by selecting "File" > "New Project Wizard."
   - Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).

2. Create a New Design File:
   - Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
   - Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

3. Write the Combinational Logic Code:
   - Open the newly created Verilog or VHDL file and write the code for your combinational logic.
     
4. Compile the Project:
   - To compile the project, click on "Processing" > "Start Compilation" in the menu.
   - Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

5. Analyze and Fix Errors: 
   - If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
   - Review and fix any issues in your code if necessary.
   - View the RTL diagram.

6. Verification:
   - Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
   - Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
   - Give the Input Combinations according to the Truth Table amd then simulate the Output Waveform.



### PROGRAM 
## code:

up counter:

![UPCOUNTER CODE](https://github.com/Rxhith1205/Exp-7-Synchornous-counters-/assets/147473311/3e63ce8f-69e7-40bd-b389-c2c404855159)

down counter:

![DOWNCOUNTER CODE](https://github.com/Rxhith1205/Exp-7-Synchornous-counters-/assets/147473311/a43f53c6-1fd2-4a43-8067-2da79f5c1e29)


### RTL LOGIC:

up counter:

![image](https://github.com/Rxhith1205/Exp-7-Synchornous-counters-/assets/147473311/0339166f-0c35-49c6-8678-30d8634ab97a)

down counter:

c![image](https://github.com/Rxhith1205/Exp-7-Synchornous-counters-/assets/147473311/2588d57b-4223-48ae-81a0-624b1a3d0ff0)



### TIMING DIGRAMS FOR COUNTER  

up counter:

![image](https://github.com/Rxhith1205/Exp-7-Synchornous-counters-/assets/147473311/4e471b88-15a8-494a-861c-de024255fc2a)


down counter:

![image](https://github.com/Rxhith1205/Exp-7-Synchornous-counters-/assets/147473311/a72c6496-153a-4e9e-9bee-424542f716ac)


### TRUTH TABLE 

up counter:

![image](https://github.com/Rxhith1205/Exp-7-Synchornous-counters-/assets/147473311/bcda0798-59dc-406d-9298-c3b3e7c1f67e)

down counter:

![image](https://github.com/Rxhith1205/Exp-7-Synchornous-counters-/assets/147473311/f81ed1e3-be66-4a87-a3ec-addd8b595d2f)


### RTL LOGIC UP COUNTER 
![image](https://github.com/Nijeesh-bit/Exp-7-Synchornous-counters-/assets/89188014/2083493c-2eec-4ade-ac68-22892f14a0cb)

### TIMING DIGRAMS FOR UP COUNTER  
<img width="790" alt="image" src="https://github.com/Nijeesh-bit/Exp-7-Synchornous-counters-/assets/89188014/972cc60c-b402-49c9-ac08-738ea2fbba02">

### TRUTH TABLE FOR UP COUNTER
<img width="287" alt="image" src="https://github.com/Nijeesh-bit/Exp-7-Synchornous-counters-/assets/89188014/c3819e0a-3ca1-498a-bbf3-fa0b70cad9ca">

### RESULTS 
By this we have verified the truth table of 4-bit up-counter using verilog.
