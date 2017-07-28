# Autonomous Snowmobile GPS #

*Lead Architect: Ryan J. Richards*

*The Pennsylvania State University - School of Electrical Engineering and Computer Science*

## Introduction ##

This repository contains GPS code for the SparkFun Venus [1]. This code utilizes MakerHub LINX VIs to read in GPS coordinates and filter them so that erroneous numbers or UART conversion mistakes do not occur.

## MakerHub LINX ##

LINX is a library developed by MakerHub that allows programmers to interface with the RaspberryPi, Arduino and other microcontrollers on LabVIEW. LINX has been used extensively in this project to communicate with the ArduinoMEGA, which controls each subsystem. Download and other information can be found at:

[MakerHub LINX](http://sine.ni.com/nips/cds/view/p/lang/en/nid/212478)


## LabVIEW Code ##

The LabVIEW code is straight-forward - UART channels are opened according to the user's input. The GPS NMEA information is read and translated. Then an additional VI is included to filter any errors.

![1](https://user-images.githubusercontent.com/23239868/28682555-6c485aec-72cb-11e7-8639-a4727b23f573.PNG)

![2](https://user-images.githubusercontent.com/23239868/28682707-f2c9e5a4-72cb-11e7-90b6-f4e554a34228.PNG)


## Hardware Setup ##

Connect the **TX0** pin to the **RX3 - PIN15** on the ArduinoMEGA (do not connect anything to **TX0** or **RX0** on the ArduinoMEGA as LINX uses these terminals).

Then, connect the **3.3V** terminal to the **3.3V** power supply on the ArduinoMEGA.

Finally, connect the **Ground** terminal to the **Ground** terminal on the ArduinoMEGA. All connections are illustrated in the figure below.

<img src="https://user-images.githubusercontent.com/23239868/28582964-71499c8c-7135-11e7-9288-09ad126642ab.jpg" height="350" width="300">

![img_0111](https://user-images.githubusercontent.com/23239868/28731649-bbcf9a44-73a2-11e7-8fa2-40e4c91b541e.JPG)


## Appendix ##

[1] [Sparkfun Venus GPS](https://www.sparkfun.com/products/11058)

[2] [Sparkfun Venus GPS manual](https://cdn.sparkfun.com/datasheets/Sensors/GPS/Venus/638/doc/Venus638FLPx_DS_v07.pdf)

