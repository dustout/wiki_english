---
name: Grove - 12-bit Magnetic Rotary Position Sensor / Encoder (AS5600)
category: 
bzurl: 
oldwikiname: 
prodimagename: 
surveyurl: 
sku: 101020692
---


![](https://raw.githubusercontent.com/SeeedDocument/Grove-12-bit-Magnetic-Rotary-Position-Sensor-AS5600/master/img/Grove-12-bit-Magnetic-Rotary-Sensor-AS5600-preview.jpg)

The Grove - AS5600 is a programmable 12-bit high-resolution contactless magnetic rotary position sensor. The Grove - AS5600 can work as a magnetic potentialmeter or a magnetic encoder with excellent realiability and durability.

Compared with the traditional potentialmeter/encoder, the Grove - AS5600 has significant advantages: high precision, non-contact, no rotation angle limitation. All those advantages making it suitable for non-contact angle measurement applications, such as the robot arm, tripod head, moter closed-loop control, machine tool axis postioning.

<p style=":center"><a href="https://www.seeedstudio.com/Grove-12-bit-Magnetic-Rotary-Position-Sensor-AS5600-p-4192.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/300px-Get_One_Now_Banner-ragular.png" /></a></p>

## Feature

- Non-contact, no rotation angle limitation
- 12-bit high-resolution, 4096 positions per round
- Grove I2C, PWM/Analog Output
- Great flexibility on angular excursion: Maximum angle programmable from 18° up to 360°

## Specification

|Parameter|Value|
|---|---|
|Supply voltage|3.3V / 5V|
|Operating ambient temperature| -40 – 125℃|
|Input Current|-100-100mA|
|Flexibility|Maximum angle programmable from 18°-360°|
|Interface|I2C(Default I2C Address: 0x36) & Non-Changeable|
|Output|Analog/PWM output|
|Output Resolution|12-bit DAC|


## Working Principle

Grove - AS5600 is based on the Hall Effect, the build-in Hall sensor can detect changes in the direction of the magnetic field, thus there is also no rotation angle limit. The magnetic field direction information is amplified by the amplifier, with the help of the build-in 12-bit A/D, the AS5600 module can output 4096 positions per round. The output is selectable, you can either use the I2C interface to output the RAW data or output the PWM wave/Analog wave via the OUT pin. Meanwhile, the maximum anlgle is also programmable, you can set the maximum angle from 18° to 360°, which means that the measured angular accuracy is up to 18/4096.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-12-bit-Magnetic-Rotary-Position-Sensor-AS5600/master/img/Grove-12-bit-Magnetic-Rotary-Sensor-AS5600-show-NS.jpg)


!!!note
    The AS5600 has certain requirements for the magnetic field to be measured. Please use a magnet similar in size to the chip. The module should be measured as close as possible to the magnetic field and the AS5600 sensor center should be aligned with the center of the magnetic field. The vertical distance is preferably from 0.5 mm to 3 mm.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-12-bit-Magnetic-Rotary-Position-Sensor-AS5600/master/img/Grove-12-bit-Magnetic-Rotary-Sensor-AS5600-2.jpg)

## Hardware Overview

<div align="center">
<figure>
  <p style=":center"><a href="https://raw.githubusercontent.com/SeeedDocument/Grove-12-bit-Magnetic-Rotary-Position-Sensor-AS5600/master/img/Grove-12-bit-Magnetic-Rotary-Sensor-AS5600-pin.jpg" target="_blank"><img src="https://raw.githubusercontent.com/SeeedDocument/Grove-12-bit-Magnetic-Rotary-Position-Sensor-AS5600/master/img/Grove-12-bit-Magnetic-Rotary-Sensor-AS5600-pin.jpg" /></a></p>
</figure>
</div>


## Platforms Supported

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |


## Getting Started

### Play With Arduino


**Materials required**


| Seeeduino V4.2 | Base Shield | Grove - 12-bit Magnetic Rotary Position Sensor / Encoder (AS5600)|
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-12-bit-Magnetic-Rotary-Position-Sensor-AS5600/master/img/Grove-12-bit-Magnetic-Rotary-Sensor-AS5600-thumbnail.jpg)
|[Get ONE Now](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Get ONE Now](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Get ONE Now](https://www.seeedstudio.com/Grove-12-bit-Magnetic-Rotary-Position-Sensor-AS5600-p-4192.html)|

>In addition, you can consider our new [Seeeduino Lotus M0+](https://www.seeedstudio.com/Seeeduino-Lotus-Cortex-M0-p-2896.html), which is equivalent to the combination of Seeeduino V4.2 and Baseshield.

#### Hardware Connection

- **Step 1.** Connect the Grove - 12-bit Magnetic Rotary Position Sensor / Encoder (AS5600) to the **I2C** port of the Base Shield.

- **Step 2.** Plug Grove - Base Shield into Seeduino.

- **Step 3** Connect the Seeeduino to PC via a USB cable.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-12-bit-Magnetic-Rotary-Position-Sensor-AS5600/master/img/HardwarePic.jpg)

#### Software

!!!Attention
        If this is the first time you work with Arduino, we strongly recommend you to see [Getting Started with Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) before the start.


- **Step 1.** Download the [AS5600](https://github.com/Seeed-Studio/Seeed_Arduino_AS5600) Library from Github.

!!!Note
        Refer How to install library to [install library](http://wiki.seeedstudio.com/How_to_install_Arduino_Library/) for Arduino.

- **Step 2.** Restart the Arduino IDE. Open **readAngle** example via the path: **File** → **Examples** → **Seeed_AS5600-master** → **readAngle**. Through this demo, we can read the angles from a magnet underneath the sensor.

The readAngle Example code is as follow:

```C++
#include <Wire.h>
#include <AS5600.h>
#ifdef ARDUINO_SAMD_VARIANT_COMPLIANCE
  #define SERIAL SerialUSB
  #define SYS_VOL   3.3
#else
  #define SERIAL Serial
  #define SYS_VOL   5
#endif

AMS_5600 ams5600;

int ang, lang = 0;

void setup()
{
  SERIAL.begin(115200);
  Wire.begin();
  SERIAL.println(">>>>>>>>>>>>>>>>>>>>>>>>>>> ");
  if(ams5600.detectMagnet() == 0 ){
    while(1){
        if(ams5600.detectMagnet() == 1 ){
            SERIAL.print("Current Magnitude: ");
            SERIAL.println(ams5600.getMagnitude());
            break;
        }
        else{
            SERIAL.println("Can not detect magnet");
        }
        delay(1000);
    }
  }
}
/*******************************************************
/* Function: convertRawAngleToDegrees
/* In: angle data from AMS_5600::getRawAngle
/* Out: human readable degrees as float
/* Description: takes the raw angle and calculates
/* float value in degrees.
/*******************************************************/
float convertRawAngleToDegrees(word newAngle)
{
  /* Raw data reports 0 - 4095 segments, which is 0.087 of a degree */
  float retVal = newAngle * 0.087;
  ang = retVal;
  return ang;
}
void loop()
{
    SERIAL.println(String(convertRawAngleToDegrees(ams5600.getRawAngle()),DEC));
}
```


- **Step 3.** Upload the demo. If you do not know how to upload the code, please check [How to upload code](http://wiki.seeedstudio.com/Upload_Code/).

- **Step 4.** Open the **Serial Monitor** of Arduino IDE by click **Tool-> Serial Monitor**. Or tap the ++ctrl+shift+m++ key at the same time. Set the baud rate to **115200**.

- **Step 5.** The result should be like this when it detected magnet underneath the sensor:

![](https://raw.githubusercontent.com/SeeedDocument/Grove-12-bit-Magnetic-Rotary-Position-Sensor-AS5600/master/img/Results.jpg)

## FAQ

**Q1#** How to achieve maximum accuracy?

**A1:** Make sure the Grove - 12-bit Magnetic Rotary Position Sensor / Encoder (AS5600) sensor is at a fixed distance/position to the magnet. Rotate the magnet to get from angle 0 all the way to angle 360 at first time to ensure positoning is correct.

The [AS5600](https://github.com/Seeed-Studio/Seeed_Arduino_AS5600) library also provides a full testing function to operate for the sensor.

## Schematic Online Viewer


<div class="altium-ecad-viewer" data-project-src="https://github.com/SeeedDocument/Grove-12-bit-Magnetic-Rotary-Position-Sensor-AS5600/raw/master/res/Grove%20-%2012-bit%20Magnetic%20Rotary%20Position%20Sensor%20(AS5600).zip" style="border-radius: 0px 0px 4px 4px; height: 500px; border-style: solid; border-width: 1px; border-color: rgb(241, 241, 241); overflow: hidden; max-width: 1280px; max-height: 700px; box-sizing: border-box;" />
</div>


## Resources

- **[ZIP]** [Grove - 12-bit Magnetic Rotary Position Sensor / Encoder (AS5600) Schematic file](https://github.com/SeeedDocument/Grove-12-bit-Magnetic-Rotary-Position-Sensor-AS5600/raw/master/res/Grove%20-%2012-bit%20Magnetic%20Rotary%20Position%20Sensor%20(AS5600).zip)
- **[PDF]** [AS5600 Datasheet](https://github.com/SeeedDocument/Grove-12-bit-Magnetic-Rotary-Position-Sensor-AS5600/raw/master/res/Magnetic%20Rotary%20Position%20Sensor%20AS5600%20Datasheet.pdf)

## Tech Support
Please submit any technical issue into our [forum](http://forum.seeedstudio.com/)<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>



