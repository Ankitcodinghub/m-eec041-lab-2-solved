# m-eec041-lab-2-solved
**TO GET THIS SOLUTION VISIT:** [M.EEC041 Lab 2 Solved](https://www.ankitcodinghub.com/product/m-eec041-lab-2-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;94393&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;M.EEC041 Lab 2 Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column"></div>
</div>
<div class="layoutArea">
<div class="column">
This project consists in implementing a digital circuit to calculate the polar coordinates of a vector, given its rectangular coordinates. The function implemented by the system can thus be summarized as:

</div>
</div>
<div class="layoutArea">
<div class="column">
Given 𝑿 and 𝒀, calculate 𝑴 = √𝑋􏰆 + 𝑌􏰆 and 𝑨 = 𝑎𝑡𝑎𝑛(𝑌􏰇𝑋)

The 𝑿 and 𝒀 inputs are fixed-point signed numbers (two’s complement), represented with 16 integer bits and 16 fractional bits. The modulus 𝑴 is positive fixed-point with 16 integer bits and 16 fractional bits and the angle 𝑨 is signed in two’s complement, with 8 bits for the integer part and 24 bits for the fractional part. The

valid input ranges for 𝑿 and 𝒀 is explained below.

The circuit implements the CORDIC algorithm (in translation mode) as a clocked

synchronous sequential digital circuit and must be built as a synthesizable Verilog module, representing exactly the logic diagram shown in figure 1. The description of the CORDIC algorithm is beyond the scope of this work, although it will be studied in detail by the end of the semester. The circuit computes the two results 𝑴 and 𝑨 by successive approximations in 32 iterations, using a total of 33 clock cycles. To execute a computation the signal enable must be set to 1 during 33 clock cycles and start must be set to 1 only in the first clock cycle to load the 𝑿 and 𝒀 operands. The testbench provided in ./src/verilog-tb/rec2pol_tb.v already includes a Verilog task to activate these control signals in the appropriate sequence.

The Verilog interface is:

<pre>   module rec2pol(
             input clock,
</pre>
<pre>             input reset,  // synchronous reset, active high
             input enable, // set and keep high to enable iteration
             input start,  // set to 1 for one clock to start
             input  signed [31:0] x,    // X component, 16Q16
             input  signed [31:0] y,    // Y component, 16Q16
             output signed [31:0] mod,  // Modulus, 16Q16
             output signed [31:0] angle // Angle in degrees, 8Q24
</pre>
);

(Note: nQm: n+m word, n bits for the integer part and m bits for the fractional part)

</div>
</div>
<div class="layoutArea">
<div class="column">
FEUP – M.EEC – M.EEC041 – Digital Systems Design 2021/22 1/3 jca@fe.up.pt

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
Figure 1 – RTL diagram of the sequential polar coordinate calculator.

2. Implementation

Download and install is your work area the zip archive with the laboratory design kit. The contents of these directories are:

</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>./doc
./matlab
</pre>
<pre>./sim
./simdata
</pre>
<pre>./src/verilog-rtl
./src/verilog-tb
./src/verilog-IPs
</pre>
</div>
<div class="column">
contains documentation related to the project, as this guide. Matlab/Octave scripts (CORDIC algorithm and generator of the datafiles located in ./simdata.

create here the QuestaSim simulation project. DO NOT use a subdirectory or the simulation will not run properly.

datafiles used for simulation, with the data to initialize the ATAN_ROM memory.

the Verilog files for implementation (or the synthesizable code). the Verilog files for building the testbench.

the provided IP cores (the gray blocks in the schematic).

</div>
</div>
<div class="layoutArea">
<div class="column">
The system must be implemented as a behavioral Verilog synthesizable module using a single clock signal for all registers, active in the positive (or rising) edge and a global synchronous reset, active high. The activation of the reset signal must set all the registers to zero.

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
The 3 shaded blocks shown in the block diagram are provided as IP cores (“Intelectual Property”) in folder ./src/Verilog-IPs. Module ATAN_ROM implements a ROM (Read-Only Memory) pre-loaded with the values of arctan􏰈2􏰉􏰊􏰋, required for the CORDICV algorithm. Module ITERCOUNTER implements a 6-bit binary counter and generates the address to the ATAN_ROM. Module MODSCALE performs a multiplication by a constant to adjust the final result generated by the CORDIC algorithm.

All the other blocks should be modeled by combinational processes using the assign or always @* statements (the adders, subtractors, multiplexers and shifters) and using sequential processes coded with the always @(posedge…) statement (the 3 registers). All registers and the block ITERCOUNTER (sequential) must be enabled by the input enable.

3. Verification

To verify your Verilog model you must adapt the testbench given and implement a convenient verification program to maximize the functional coverage of your code. The task execcordic already included in the testbench implements the correct sequence of signals start and enable to perform a rectangular to polar conversion, including a text output statement ($display()) to print the results in fractional decimal. Improve the testbench in order to automate the verification procedure.

4. Additional developments

4.1 The current implementation only performs correctly for vectors in the 1st and 4th quadrants (𝑿 positive and output angle in the range [-90o , +90o]). Without modifying the initial implementation, create a new module that allows the rectangular to polar conversion along the 4 quadrants. The new module should instantiate the rec2pol module and implement the additional functionality, using at most one additional clock cycle.

4.2 The present implementation requires the external circuit to keep the enable signal high while the iterative process is running (during exactly 33 clock cycles). Make a new version of the ITERCOUNTER block that generates internally the signal enable for itself and for the 3 registers and outputs a new signal ready meaning the system is able to initiate a new computation. While the computation is begin performed, ready should be set to zero. This new module should receive only the start pulse, set to 1 during a single clock period. Additionally, if a computation is running (ready==0) the input start must be ignored.

</div>
</div>
</div>
