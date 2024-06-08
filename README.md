# pygate
PyGate is a wrapped API providing functions adapted for use in a Pythonic manner with AnaGate libraries. The AnaGate product line comprises various hardware devices offering access to different bus systems (such as I2C, SPI, CAN). An AnaGate device functions as a TCP server, establishing a socket with its IP address and a device-specific port number. Access to the different models of the AnaGate product line is consistently achieved through the widely used TCP network protocol.

However, the library interface of the AnaGate API is implemented in the programming language C ([Chapter 3. Common function reference](http://www.anagate.de/download/Manual-AnaGateAPI2-en.pdf)), presenting a challenge for Python users.

## Package Structure
1. The directory [/AnagateCAN/AnaGateAPI-CAN-1.11-2.13](https://github.com/ahmedqamesh/AnagateCAN/tree/master/AnaGateAPI-CAN-1.11-2.13) includes:</br>
a. The [AnaGate API for Windows (32/64 bit)](http://www.anagate.de/download/API/AnaGateAPI-SPI-1.3-2.13.zip).</br>
b. The [AnaGate API for Linux X86 (32/64bit)](http://www.anagate.de/download/API/AnaGateAPI-SPI-1.3-2.13.tar.bz2).</br>

2. The directory [includes](https://github.com/ahmedqamesh/AnagateCAN/tree/master/analib/include) :Where all the header files from AnaGate API Software in C exist.</br>
3. The directory [lib](https://github.com/ahmedqamesh/AnagateCAN/tree/master/analib/include) : Where all library files from AnaGate API Software exist.</br>
4. The communication with the CAN bus Transmit/Receive command uses the function write in [channel.py](https://github.com/ahmedqamesh/AnagateCAN/blob/master/analib/channel.py) to transmit a CAN message to the CAN bus via the AnaGate device based on two main arguments: COB_ID and data.


### Getting Started
Clone the repository to download the source code:
```
git@github.com:ahmedqamesh/AnaGateAPI-CAN-Py.git
```
Ensure the CAN interface is connected and the required software is installed. To test the setup, run the following command in the home directory:

```
python test_SDO.py
```


## Contributing and Contact Information:
We welcome contributions from the community please contact : `ahmed.qamesh@cern.ch`.
