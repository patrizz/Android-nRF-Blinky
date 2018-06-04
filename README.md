# nRF BLINKY

nRF Blinky is an application developed targeting an audience of developers who are new to Bluetooth Low Energy. 
This is a very simple application with two basic features to turn on LED 1 on the nRF DK and to recieve the Button 1 press event from 
a nRF DK on the nRF Blinky Application.
It demonstrates how to use the **BleManager** class from [Android nRF Blinky](https://github.com/NordicSemiconductor/Android-BLE-Library/) 
library can be used from View Model (see [Architecture Components](https://developer.android.com/topic/libraries/architecture/index.html)).

### Nordic LED and Button Service

Service UUID: `00001523-1212-EFDE-1523-785FEABCD123`

A simplified proprietary service by Nordic Semiconductor, containing two characteristics one to control LED 3 and Button 1:

- First characteristic controls the LED state (On/Off).
  - UUID: **`00001525-1212-EFDE-1523-785FEABCD123`**
  - Value: **`1`** => LED On
  - Value: **`0`** => LED Off

- Second characteristic notifies central of the button state on change (Pressed/Released).
  - UUID: **`00001524-1212-EFDE-1523-785FEABCD123`**
  - Value: **`1`** => Button Pressed
  - Value: **`0`** => Button Released

### Requirements

* ~~In order to compile the project you have to clone [Android BLE Library](https://github.com/NordicSemiconductor/Android-BLE-Library/) 
to the same root folder (for example into AndroidstudioProjects).~~ Since version 2.1.0 the app imports the BLE Library from jcenter.

* Android 4.3 or newer is required.

### Installation and usage

Prepare your Development kit.
  - Plug in the Development Kit to your computer via USB.
  - Power On the Development Kit.
  - The Development Kit will now appear as a Mass storage device.
  - Drag (or copy/paste) the appropriate HEX file onto that new device.
  - The Development Kit lEDS will flash and it will disconnect and reconnect.
  - The Development Kit is now ready and flashed with the nRFBlinky example firmware.

For your convenience, we have bundled two firmwares in this project under the Firmwares directory.

To get the latest firmwares and check the source code, you may go directly to our [Developers website](http://developer.nordicsemi.com/nRF5_SDK/) 
and download the SDK version you need, then you can find the source code and hex files to the blinky demo in the directory `/examples/ble_peripheral/ble_app_blinky/`.

More information about the nRF Blinky example firmware can be found in the 
[Infocenter](https://infocenter.nordicsemi.com/index.jsp?topic=%2Fcom.nordic.infocenter.sdk5.v14.2.0%2Fble_sdk_app_blinky.html).

### Note

In order to scan for Bluetooth LE device the Location permission must be granted and, on some phones, the Location must be enabled. 
This app will not use the location information in any way.
