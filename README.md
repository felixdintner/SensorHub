# SensorHub
Calumino's door counting and people counting solution

The Calumino Sensor Hub is a device employing the Calumino thermal sensor (CTS), combined with on-edge processing and network connectivity for Internet of Things (IoT) applications.
The Calumino Sensor Hub is a multi-use sensor, performing functions such as people detection, people counting, people tracking, fall detection and other human activity monitoring in smart buildings, mission critical infrastructure, security applications, aged care/hospitals and more. By detecting only heat signatures in low-resolution, the Sensor Hub is 100% privacy non-intrusive.

![Use cases](/Docs/Images/use_cases.png)

As per diagram below, the low-res Infrared images from the CTS are processed on-edge using Calumino's proprietary Computer Vision pipeline architecture. The Azure IoT SDK receives the count data out of the pipelines and transmits it to Azure IoT Hub.

![Architecture](/Docs/Images/architecture.png)

## How to order a CTS
The Calumino Sensor Hub can be ordered via our customer service desk at [Contact us - Calumino](https://calumino.com/contact-us/) or info@calumino.com.
It is also possible to order a standalone CTS starter kit to develop custom end user devices and applications.

## Getting Started
1. Once you have received the CTS starter kit, please follow these instructions to connect the devices to the IoT Hub: [Create an IoT hub using the Azure portal](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-create-through-portal)

2. Once you have received the connection string, please visit the settings page is available at: `http://{ip_address}:1234` or `http://{hostname}.local:1234`   
{ip_address} and {hostname} can be obtained from a local ip scanner software.

3. Please paste the connection string into the relevant section on the settings page:

![Settings page](/Docs/Images/settings.png)

4. Here an example of the payload being transmitted by the device to the Azure IoT Hub:
```bash
{"schema": "CALUMINO_V2", "utcMSecs": 1642738249209, "data": {"eventType": "EVT_IM_ALIVE", "serialNum": "0000f2297a64", "mac": "dca632b0f7fd", "hwVer": 537276672, "swVer": 537469696, "peopleCount": 0, "visibleCount": 0, "currentEnter": 0, "currentExit": 0, "relativeCount": 0, "areaCounters": {}, "bootUptimeSecs": 145348}}
```
