Download Link: https://assignmentchef.com/product/solved-ve270-assignment-4-design-of-a-counter
<br>
<h2>Objectives</h2>

<ul>

 <li>To understand and design a special FSM – Counter.</li>

 <li>To design the counter by HDL modeling</li>

 <li>To experience the development process of an FPGA based digital device using HDL.</li>

 <li>2. Requirement</li>

</ul>

In this lab, you are to design a device commonly used in modern computers, a 4-bit up/down synchronous binary counter. The counter is defined as follows:

<ul>

 <li>A 4-bit binary counter uses 4 flip-flop outputs to represent a binary number. It is capable of counting from 0 to 15.</li>

 <li>A synchronous counter implies that all flip-flops are sharing the same clock signal.</li>

 <li>An up/down counter is capable of counting up (incrementing) or down (decrementing).</li>

</ul>




The counter has two 1-bit control inputs called “Up/Down” and “Reset”. The counter is to increment if “Up/Down” is 1 and decrement if “Up/Down” is 0. When “Reset” is 1 the counter should go to 0 no matter what the other inputs might be. “Up/Down” input can be provided with a toggle switch. The “Reset” input can be provided with a push button. Another input to the counter is “Clock”. Rising edges of “Clock” should trigger increment or decrement of the counter.




Model the 4-bit up/down synchronous binary counter with Verilog HDL.




The outputs of the counter should be captured with 4 LEDs on the FPGA board, <strong>and also supplied to an SSD Driver modeled with Verilog HDL so that the binary number is displayed in its hexadecimal equivalent</strong>.




<strong>NOTE</strong>: the “Clock” signal can be connected to a push button or any other regular input source directly. Thus, each button press produces a rising edge.




<h2>3. Setting up Xilinx Vivado</h2>




In this section, you will set up the Xilinx Vivado digital system development environment and get it ready for circuit simulation and implementation.




<ul>

 <li>Click on the icon to open the Vivado software.</li>

 <li>Click “Create Project” in the left side panel shown below or from the drop down menu: File à New Project;</li>

</ul>










<ul>

 <li>Follow the navigator to choose project file location and project name;</li>

</ul>







<ul>

 <li>Select “RTL Project” option in the Project Type window, and Next;</li>

</ul>







You could check “Do not specify sources at this time” box if you want to add source file later.

<ul>

 <li>Add Sources (skip for now)</li>

 <li>Add Constrains (skip for now)</li>

 <li>Choose Default Part. There are two ways to choose parts, select by Parts or by Boards: a. Select by Parts:</li>

</ul>

Search and Choose parts: <strong>XC7A35TCPG236-1</strong>

<ol>

 <li>Select by Boards:

  <ol>

   <li>Download Digilent Vivado boards file from <u>com</u>.</li>

   <li>Copy folders in “new/board_files” into “vivado install location/Vivado/version/data/boards/board_files”. For detail, please refer to the instruction on <u>Digilent website</u>.</li>

  </ol></li>

</ol>

<ul>

 <li>You will find board file for Basys3</li>

</ul>







<ul>

 <li>Finish</li>

</ul>




Now a new project is created in the Vivado software.




<ul>

 <li>Find “Sources” window and click “+” to add or create source;</li>

</ul>










<ul>

 <li>Choose “Add or create design sources”; Next;</li>

</ul>










<ul>

 <li>Click “Create File”</li>

 <li>Choose “File type” to be Verilog, enter File name.</li>

</ul>










<ul>

 <li>Click “OK” and “Finish”; then a “Define Module” window will pop up. You can skip this step, or you can also name your module ports here;</li>

 <li>Write Verilog code in the file to implement your design;</li>

</ul>

Repeat steps 9) to 14) to create multiple source files;