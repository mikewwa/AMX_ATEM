# AMX_ATEM

This is an include file that works on an AMX Netlinx Studio to control ATEM switchers. It currrently only been tested with a ATEM Television Studio.  I have tested the include file on both an NI and NX series processor.  The ATEM protocol seems to be timing sensitive, so you may run into issues if the controller this is running on is to busy to responed in a timely manner to the ACK requests.  It supports basic functionalitly, like changing the program or preview input, doing a cut, getting input long and shor names, getting the model and version.

The include file is a port of the Blackmagic Design ATEM Client library for Arduino by 
Kasper Skårhøj, SKAARHOJ K/S, kasper@skaarhoj.com 
It can be found here:  https://github.com/kasperskaarhoj/SKAARHOJ-Open-Engineering/tree/master/ArduinoLibs



Include file that contains the main ATEM switcher code
- ATEM Switcher.axi

It has only been tested with an ATEM Television Studio.

	
Touch panel demo:
- ATEM Switcher Demo.axs
- ATEM Demo.TP4 (for an MST-701)

Panel looks simlar to the ATEM Software Control system and supports selecting inputs for program and preview along with cutting.  It will also display the the switchers model, version, ip address and output resolution along with the short names for the inputs.

DGX style switching of a ATEM Television Studio using M2M virtual device communication
- ATEM Switcher-dgx.axs

Supports some of the DGX switching commands:
- CI\<input\>O\<output\>  output 1 is program, output 2 is preview, output 0 will trigger a cut
- ?MODEL
- ?OUTPUT-VIDEO
- ?VIDOUT_RES_REF
- ?ATEM:ONLINE
- ATEM:ONLINE
- ATEM:OFFLINE
- ?VIDIN_NAME


