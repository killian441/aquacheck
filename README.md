AquaCheck
===========

This contains a block used with the AquaCheck soil moisture probe over a serial interface. Some models of the AquaCheck probe accept RS485 input, and this block supports that. Other models of the probe use the one wire SDI-12 protocol and this block supports this natively with the required hardware fix (inverting and tying the TX and RX lines of the uart together). 

Properties
--------------
signalName - Name of the emitted signal
portNumber - UART port location (ie '/dev/ttymxc4')
sendMarking - Send marking? SDI-12 protocol specifies a marking signal should be sent to wake up sensors on the line, but not required for the RS485 version of the probe.
rs485 - Enable RS485 protocol on the UART (not required on a USB adapter)

Dependencies
----------------
The aquacheck_block requires pySerial and Tenacity.

Commands
----------------
None

Input
-------
Any list of signals.

Output
---------
Some list of signals as input.
