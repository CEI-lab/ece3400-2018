# FPGA-related resources: useful tips and links

We are using the DE0-Nano development board. 

## DE0-Nano User manual

User manuals or data sheets are the best resources when working with new hardware. Download the user manual for DE0-Nano [here](https://www.terasic.com.tw/cgi-bin/page/archive_download.pl?Language=English&No=593&FID=75023fa36c9bf8639384f942e65a46f3). To familiarize yourself with the board layout, we recommend reading through Chapter 2 (it's short and mostly contains pictures). Since we will mainly be interacting with the on-board pushbuttons, LEDs, and switches, we also recommend taking a look at Chapter 3.2, which contains details about user input/output including the pinout for the GPIO pins.

## Quartus

## Verilog

Verilog is a hardware description language (HDL), which means that all the code you write for the FPGA in Verilog represents combinational or sequential logic in hardware. During compiliation, Quartus must analyze all the logic you've written and determine how to best synthesize it onto the FPGA; this is the reason why compile times are so much longer than software compile times. When writing Verilog, it's important to understand the hardware behind your code, as this will help you to consider important logic errors. For example, signals in Verilog can be one of two data types: a _reg_ (variable data type) or a _wire_ (net data type). _Wires_ can only be used to model combinational logic and they cannot store values. _Regs_ represent data storage elements and can be used to model both combinational and sequential logic in _always_ blocks. For many more details on Verilog syntax, check out the Verilog Quick Reference Guide [here](http://sutherland-hdl.com/pdfs/verilog_2001_ref_guide.pdf).

