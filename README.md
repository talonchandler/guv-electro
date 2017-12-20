# guv-electro

Electroformation script for controlling an Agilent 33120A to create giant unilamellar vesicles (GUV). See [this protocol](http://www.sciencedirect.com/science/article/pii/S0091679X15000679?via%3Dihub) for details.

The script generate a 
1. 30 minute sine at 10 Hz ramping linearly from 0.05 to 1.41 Vpp
2. 120 minute sine at 10 Hz at 1.41 Vpp
3. 30 minute square at 4.5 Hz at 2.12 Vpp.

## Installation 

Install Python 3.
Use pip to install `numpy`, and `pyserial`. 
Modify script path to find interpreter.
Modify serial port `COMX` on Windows and `/dev/ttyXXX` otherwise.

Example usage:

    ./guv-electro

Test script (argument multiplies total time):

    ./guv-electro 0.01