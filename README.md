# guv-electro

Electroformation script for controlling an Agilent 33120A to create giant unilamellar vesicles (GUV). See [this protocol](http://www.sciencedirect.com/science/article/pii/S0091679X15000679?via%3Dihub) for details.

The script generates a 
1. 30 minute sine at 10 Hz ramping linearly from 0.05 to 1.41 Vpp
2. 120 minute sine at 10 Hz at 1.41 Vpp
3. 30 minute square at 4.5 Hz at 2.12 Vpp.

## Find IP address from raspberry pi

    hostname -I   

## SSH into raspberry pi from any computer on MBL-GUEST

    ssh pi@10.208.2.178 (your IP address here)
    password: polscope

    cd guv-electro
    ./guv-electro

## Example usage

    ./guv-electro

Test script (argument multiplies the total run time):

    ./guv-electro 0.01

Run with no hangups, log the output, and tail the log file

    ./run-guv

Watch the output

    tail -f nohup.out

To quit the job midway through, find the PID of the python process and kill it

    ps
    kill PID

## Installation 

Install Python 3.  Use `pip` to install `numpy` and `pyserial`.  Modify the
script path to find interpreter.  Modify the serial port path to find the
function generator. Use `COMX` on Windows and `/dev/ttyXXX` otherwise.


