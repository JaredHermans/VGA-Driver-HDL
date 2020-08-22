# VGA-Driver-HDL
Project outputs image test patterns to a VGA monitor. The test patterns are selectable by the computer keybord which communitates to the Go Board via Putty and UART. 
ASCI values of the keyboard strokes are displayed on the 7-Segment displays in hex.

**VGA_Test_Patterns_Top** is the top level module that calles the UART Reciever, UART Transmitter, Binary to 7 segment converter, Sync pulse generator, test pattern
generator, and VGA Sync Porch. 

**VGA_Test_Patterns_TB** is the testbench that verifies VGA_Sync_Pulses, Test_Patter_Gen, Sync_To_Count, and VGA_Sync_Porch. Modelsim waveform image also shown.

**Test_Pattern_Gen** module generates 6 different patterns on the VGA display simultaneously and value of i_Pattern determines which one is displayed.

**VGA_Sync_Pulses** generates HSync and VSync without the front porch or back porch for VGA driver.

**Sync_To_Count** takes HSync and VSync as inputs and outputs them along with a vertical and horizontal counter to keep track of where you are in the frame.

**VGA_Sync_Porch** modifies HSync and VSync to include the front porch and back porch.
