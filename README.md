Create CAN_python_scanner
PURPOSE:  You have unknown CAN hardware device which you wanna control but don't have any docs or addresses or data.
(Digital speedometer / tachometer / etc)

First you wanna find out working CAN speed of the device by using software coming with your adapter. At the right speed device must send some data upon start.

This script working with CAN adapters like Canable, MKS Canable with SLCAN firmware via virtual COM port interface.
Python environment must be installed first with necessary dependencies:
pip install python-can
You can use it even in windows (my case)

Connect device you wanna research to CAN adapter, set your COM port in script.
Address ID range you can change also right inside script.

After launch script:
python script.py

Input 4 bytes range in DEC for scan:
0-255 (00-FF), etc. and hit Enter

Script will scan step by step all data for all address range.

For better reaction - you can use delay in seconds "time.sleep(0.0001)" inside script.

!!! WARNING !!! During reverse engineering be careful and use it on your own risk. Some devices have registers which can turn on programming or DFU mode and you will not able back them.
