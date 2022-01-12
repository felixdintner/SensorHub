# SensorHub
Calumino's door counting and people counting solution

The Calumino Sensor Hub is a device employing the Calumino thermal sensor (CTS), combined with on-edge processing and network connectivity for Internet of Things (IoT) applications.
The Calumino Sensor Hub is a multi-use sensor, performing functions such as people detection, people counting, people tracking, fall detection and other human activity monitoring in smart buildings, mission critical infrastructure, security applications, aged care/hospitals and more. By detecting only heat signatures in low-resolution, the Sensor Hub is 100% privacy non-intrusive.

![Use cases](/Docs/Images/use_cases.png)

As per diagram below, the low-res Infrared images from the CTS are processed on-edge using Calumino's proprietary Computer Vision pipeline architecture. The Azure IoT SDK receives the count data out of the pipelines and transmits it to Azure IoT Hub. 

![Architecture](/Docs/Images/architecture.png)