# VGA-Driver-HDL

Project outputs image test patterns to a VGA monitor. The test patterns are selectable by the computer keybord which communitates to the Go Board via Putty and UART. 
ASCI values of the keyboard strokes are displayed on the 7-Segment displays in hex.

VGA_Test_Patterns_Top is the top level module that calles the UART Reciever, UART Transmitter, Binary to 7 segment converter, Sync pulse generator, test pattern
generator, and VGA Sync Porch. 

VGA_Test_Patterns_TB is the testbench that verifies VGA_Sync_Pulses, Test_Patter_Gen, Sync_To_Count, and VGA_Sync_Porch. Modelsim waveform image also shown.
