---
id: overwolf-logitech-led
title: overwolf.logitech.led API
sidebar_label: overwolf.logitech.led
---

Provides API for Logitech Arx Control.

## Methods Reference

* [`init()`](#initcallback)
* [`setTargetDevice()`](#settargetdevicetargetdevices-callback)
* [`saveCurrentLighting()`](#savecurrentlightingcallback)
* [`setLighting()`](#setlightingredpercentage-greenpercentage-bluepercentage-callback)
* [`restoreLighting()`](#restorelightingcallback)
* [`flashLighting()`](#flashlightingredpercentage-greenpercentage-bluepercentage-millisecondsduration-millisecondsinterval-callback)
* [`pulseLighting()`](#pulselightingredpercentage-greenpercentage-bluepercentage-millisecondsduration-millisecondsinterval-callback)
* [`stopEffects()`](#stopeffectscallback)
* [`setLightingFromBitmap()`](#setlightingfrombitmapbitmapurl-callback)
* [`setLightingFromBitmap()`](#setlightingfrombitmapbitmap-callback)
* [`setLightingForKeyWithScanCode()`](#setlightingforkeywithscancodekeycode-redpercentage-greenpercentage-bluepercentage-callback)
* [`setLightingForKeyWithHidCode()`](#setlightingforkeywithhidcodekeycode-redpercentage-greenpercentage-bluepercentage-callback)
* [`setLightingForKeyWithQuartzCode()`](#setlightingforkeywithquartzcodekeycode-redpercentage-greenpercentage-bluepercentage-callback)
* [`setLightingForKeyWithKeyName()`](#setlightingforkeywithkeynamekeyname-redpercentage-greenpercentage-bluepercentage-callback)
* [`saveLightingForKey()`](#savelightingforkeykeyname-callback)
* [`restoreLightingForKey()`](#restorelightingforkeykeyname-callback)
* [`flashSingleKey()`](#flashsinglekeykeyname-redpercentage-greenpercentage-bluepercentage-millisecondsduration-millisecondsinterval-callback)
* [`pulseSingleKey()`](#pulsesinglekeykeyname-startredpercentage-startgreenpercentage-startbluepercentage-finishredpercentage-finishgreenpercentage-finishbluepercentage-millisecondsduration-isinfinite-callback)
* [`stopEffectsOnKey()`](#stopeffectsonkeykeyname-callback)
* [`shutdown()`](#shutdown)

## Events Reference

* [`onError`](#onerror)

## Types Reference

* [`overwolf.logitech.led.LogitechLedData`](#overwolflogitechledlogitechleddata-object) Object
* [`overwolf.logitech.led.LogitechArxData`](#overwolflogitechledlogitecharxdata-object) Object
* [`overwolf.logitech.led.enums.LogitechDeviceLightingType`](#overwolflogitechledenumslogitechdevicelightingtype-enum) enum
* [`overwolf.logitech.led.enums.KeyboardNames`](#overwolflogitechledenumskeyboardnames-enum) enum

## init(callback)
#### Version added: 0.93

> Initializes the LED API.

Parameter    | Type     | Description                                          |
------------ | ---------| ---------------------------------------------------- |
callback     | function | A callback with the result of the request            |

## setTargetDevice(targetDevices, callback)
#### Version added: 0.93

> Sets the target devices to use.

Parameter    | Type     | Description                                          |
------------ | ---------| ---------------------------------------------------- |
targetDevices| [overwolf.logitech.led.enums.LogitechDeviceLightingType](#overwolflogitechledenumslogitechdevicelightingtype-enum) array |            |
callback     | function | A callback with the result of the request            |

## saveCurrentLighting(callback)
#### Version added: 0.93

> Saves the current lighting.

Parameter    | Type     | Description                                          |
------------ | ---------| ---------------------------------------------------- |
callback     | function | A callback with the result of the request            |

## setLighting(redPercentage, greenPercentage, bluePercentage, callback)
#### Version added: 0.93

> Sets the lighting for the entire device.

Parameter       | Type     | Description                                          |
--------------  | ---------| ---------------------------------------------------- |
redPercentage   | int      | Red percentage (0 – 100)                             |
greenPercentage | int      | Green percentage (0 – 100)                           |
bluePercentage  | int      | Blue percentage (0 – 100)                            |
callback        | function | A callback with the result of the request            |

## restoreLighting(callback)
#### Version added: 0.93

> Restores the lightning to the last previously saved state.

Parameter    | Type     | Description                                          |
------------ | ---------| ---------------------------------------------------- |
callback     | function | A callback with the result of the request            |

## flashLighting(redPercentage, greenPercentage, bluePercentage, milliSecondsDuration, milliSecondsInterval, callback)
#### Version added: 0.93

> Flashes the lighting on the device.

Parameter             | Type     | Description                                          |
--------------------  | ---------| ---------------------------------------------------- |
redPercentage         | int      | Red percentage (0 – 100)                             |
greenPercentage       | int      | Green percentage (0 – 100)                           |
bluePercentage        | int      | Blue percentage (0 – 100)                            |
milliSecondsDuration  | int      | The duration to flash in milliseconds                |
milliSecondsInterval  | int      | The interval for flashes in milliseconds             |
callback              | function | A callback with the result of the request            |

## pulseLighting(redPercentage, greenPercentage, bluePercentage, milliSecondsDuration, milliSecondsInterval, callback)
#### Version added: 0.93

> Pulses the lighting on the device.

Parameter             | Type     | Description                                          |
--------------------  | ---------| ---------------------------------------------------- |
redPercentage         | int      | Red percentage (0 – 100)                             |
greenPercentage       | int      | Green percentage (0 – 100)                           |
bluePercentage        | int      | Blue percentage (0 – 100)                            |
milliSecondsDuration  | int      | The duration to flash in milliseconds                |
milliSecondsInterval  | int      | The interval for flashes in milliseconds             |
callback              | function | A callback with the result of the request            |

## stopEffects(callback)
#### Version added: 0.93

> Stops ongoing pulse/flash effects.

Parameter    | Type     | Description                                          |
------------ | ---------| ---------------------------------------------------- |
callback     | function | A callback with the result of the request            |

## setLightingFromBitmap(bitmapUrl, callback)
#### Version added: 0.93

> Sets the lighting from an overwolf-extension:// or overwolf-media:// url. The file must be 21×6.

Parameter    | Type     | Description                                          |
------------ | ---------| ---------------------------------------------------- |
bitmapUrl	 | string   | The Overwolf url to add                              |
callback     | function | A callback with the result of the request            |

## setLightingFromBitmap(bitmap, callback)
#### Version added: 0.93

> Sets the lighting from a bitmap byte array.

Parameter    | Type     | Description                                          |
------------ | ---------| ---------------------------------------------------- |
bitmap		 | Byte[]   | A byte array representing a 21×6 bitmap              |
callback     | function | A callback with the result of the request            |

## setLightingForKeyWithScanCode(keyCode, redPercentage, greenPercentage, bluePercentage, callback)
#### Version added: 0.93

> Sets the lighting for a specific key by scan code.

Parameter             | Type     | Description                                          |
--------------------  | ---------| ---------------------------------------------------- |
keyCode	              | int      | The key scan code                                    |
redPercentage         | int      | Red percentage (0 – 100)                             |
greenPercentage       | int      | Green percentage (0 – 100)                           |
bluePercentage        | int      | Blue percentage (0 – 100)                            |
callback              | function | A callback with the result of the request            |

## setLightingForKeyWithHidCode(keyCode, redPercentage, greenPercentage, bluePercentage , callback)
#### Version added: 0.93

> Sets the lighting for a specific key by HID code.

Parameter             | Type     | Description                                          |
--------------------  | ---------| ---------------------------------------------------- |
keyCode	              | int      | The key HID code                                     |
redPercentage         | int      | Red percentage (0 – 100)                             |
greenPercentage       | int      | Green percentage (0 – 100)                           |
bluePercentage        | int      | Blue percentage (0 – 100)                            |
callback              | function | A callback with the result of the request            |

## setLightingForKeyWithQuartzCode(keyCode, redPercentage, greenPercentage, bluePercentage, callback)
#### Version added: 0.93

> Sets the lighting for a specific key by HID code.

Parameter             | Type     | Description                                          |
--------------------  | ---------| ---------------------------------------------------- |
keyCode	              | int      | The key quartz  code                                 |
redPercentage         | int      | Red percentage (0 – 100)                             |
greenPercentage       | int      | Green percentage (0 – 100)                           |
bluePercentage        | int      | Blue percentage (0 – 100)                            |
callback              | function | A callback with the result of the request            |

## setLightingForKeyWithKeyName(keyName, redPercentage, greenPercentage, bluePercentage, callback)
#### Version added: 0.93

> Sets the lighting for a specific key by key name.

Parameter             | Type     | Description                                          |
--------------------  | ---------| ---------------------------------------------------- |
keyName	              | [overwolf.logitech.led.enums.KeyboardNames](#overwolflogitechledenumskeyboardnames-enum) enum      | The key name       |
redPercentage         | int      | Red percentage (0 – 100)                             |
greenPercentage       | int      | Green percentage (0 – 100)                           |
bluePercentage        | int      | Blue percentage (0 – 100)                            |
callback              | function | A callback with the result of the request            |

## saveLightingForKey(keyName, callback)
#### Version added: 0.93

> Saves the current lighting of a specific key.

Parameter             | Type     | Description                                          |
--------------------  | ---------| ---------------------------------------------------- |
keyName	              | [overwolf.logitech.led.enums.KeyboardNames](#overwolflogitechledenumskeyboardnames-enum) enum | The key name    |
callback              | function | A callback with the result of the request            |

## restoreLightingForKey(keyName, callback)
#### Version added: 0.93

> Restores a previously saved lighting for a specific key.

Parameter             | Type     | Description                                          |
--------------------  | ---------| ---------------------------------------------------- |
keyName	              | [overwolf.logitech.led.enums.KeyboardNames](#overwolflogitechledenumskeyboardnames-enum) enum | The key name    |
callback              | function | A callback with the result of the request            |

## flashSingleKey(keyName, redPercentage, greenPercentage, bluePercentage, milliSecondsDuration, milliSecondsInterval, callback)
#### Version added: 0.93

> Flashes a single key.

Parameter             | Type     | Description                                          |
--------------------  | ---------| ---------------------------------------------------- |
keyName	              | [overwolf.logitech.led.enums.KeyboardNames](#overwolflogitechledenumskeyboardnames-enum) enum      | The key name       |
redPercentage         | int      | Red percentage (0 – 100)                             |
greenPercentage       | int      | Green percentage (0 – 100)                           |
bluePercentage        | int      | Blue percentage (0 – 100)                            |
milliSecondsDuration  | int      | The duration to flash in milliseconds                |
milliSecondsInterval  | int      | The interval for flashes in milliseconds             |
callback              | function | A callback with the result of the request            |

## pulseSingleKey(keyName, startRedPercentage, startGreenPercentage, startBluePercentage, finishRedPercentage, finishGreenPercentage, finishBluePercentage, milliSecondsDuration, isInfinite, callback)
#### Version added: 0.93

> Pulses a single key.

Parameter            | Type                                                                                           | Description                              |
-------------------- | -----------------------------------------------------------------------------------------------| -----------------------------------------|
keyName	             | [overwolf.logitech.led.enums.KeyboardNames](#overwolflogitechledenumskeyboardnames-enum) enum  | The key name                             |
startRedPercentage	 | int                                                                                            | Red start percentage (0 – 100)           |
startGreenPercentage | int                                                                                            | Green start percentage (0 – 100)         |
startBluePercentage	 | int                                                                                            | Blue start percentage (0 – 100)          |
finishRedPercentage	 | int                                                                                            | Red finish percentage (0 – 100)          |
finishGreenPercentage| int                                                                                            | Green finish percentage (0 – 100)        |
finishBluePercentage | int                                                                                            | Blue finish percentage (0 – 100)         |
milliSecondsDuration | int                                                                                            | The duration to flash in milliseconds    |
milliSecondsInterval | int                                                                                            | The interval for flashes in milliseconds |
callback             | function                                                                                       | A callback with the result of the request|

## stopEffectsOnKey(keyName, callback)
#### Version added: 0.93

> Stops ongoing pulse/flash effects on a specific key.

Parameter             | Type                                                                                             | Description                              |
--------------------  | ----------------------------------------------------------------------------------------------| ------------------------------------------- |
keyName	              | [overwolf.logitech.led.enums.KeyboardNames](#overwolflogitechledenumskeyboardnames-enum) enum | The key name                                |
callback              | function                                                                                       | A callback with the result of the request  |

## shutdown()
#### Version added: 0.93

> Shuts down the API.

## onError

#### Version added: 0.93

> Triggered when an error occurs, sent with an error code.

## overwolf.logitech.led.LogitechLedData Object
#### Version added: 0.93

> Describes an Arx event.

Parameter                | Type                                                             | Description                   |
------------------------ | -----------------------------------------------------------------| ----------------------------- |
required_devices         | [LogitechDevice](overwolf-logitech#logitech-device-object) Objet | A list of required devices    |
required_devices_details | string                                                           | Read only. The list of required devices with additional details   |
required_lighting_types  | [LogitechDeviceLightingType](#overwolflogitechledenumslogitechdevicelightingtype-enum) enum    | A list of required lighting types  |
required_lighting_details| string                                                           | The value string on the event |


## overwolf.logitech.led.LogitechArxData Object
#### Version added: 0.93

> Describes the Arx API data.

Parameter   | Type   | Description                                            |
------------| -------| ------------------------------------------------------ |
app_folder  | string | An optional folder to use when publishing a website    |

## overwolf.logitech.led.enums.LogitechDeviceLightingType enum
#### Version added: 0.93

> A list of Logitech devices lighting types.

Parameter   |  Description|
------------| ----------- |
Mono        |             |
RGB         |             |
PerkeyRGB   |             |
All         |             |

## overwolf.logitech.led.enums.KeyboardNames enum
#### Version added: 0.93

> The names of the keys.

Parameter  |  Description|
-----------| ----------- |
ESC        |             |
F1         |             |
F2         |             |
F3         |             |
F4         |             |
F5         |             |
F6         |             |
F7         |             |
F8         |             |
F9         |             |
F10        |             |
F11        |             |
F12        |             |
PRINT_SCREEN        |             |
SCROLL_LOCK         |             |
PAUSE_BREAK         |             |
TILDE         |             |
ONE         |             |
TWO         |             |
THREE         |             |
FOUR         |             |
FIVE         |             |
SIX         |             |
SEVEN        |             |
EIGHT        |             |
NINE        |             |
ZERO         |             |
MINUS         |             |
EQUALS         |             |
BACKSPACE         |             |
INSERT         |             |
HOME         |             |
SPAGE_UPEVEN        |             |
NUM_LOCK        |             |
NUM_SLASH        |             |
NUM_ASTERISK        |             |
NUM_MINUS        |             |
NINE        |             |
ZERO         |             |
MINUS         |             |
TAB         |             |
Q         |             |
W        |             |
HOME         |             |
E        |             |
R       |             |
T        |             |
Y        |             |
U       |             |
I       |             |
O      |             |
P       |             |
OPEN_BRACKET         |             |
CLOSE_BRACKET         |             |
BACKSLASH         |             |
KEYBOARD_DELETE         |             |
END        |             |
PAGE_DOWN         |             |
NUM_SEVEN        |             |
NUM_EIGHT       |             |
NUM_NINE        |             |
NUM_PLUS      |             |
CAPS_LOCK      |             |
I       |             |
O      |             |
P       |             |
A         |             |
S        |             |
D         |             |
F        |             |
G       |             |
H        |             |
J      |             |
K      |             |
L       |             |
SEMICOLON      |             |
APOSTROPHE       |             |
ENTER         |             |
NUM_FOUR         |             |
NUM_FIVE         |             |
NUM_SIX         |             |
LEFT_SHIFT        |             |
Z         |             |
X        |             |
C       |             |
V        |             |
B      |             |
N      |             |
M       |             |
COMMA      |             |
PERIOD       |             |
FORWARD_SLASH        |             |
RIGHT_SHIFT       |             |
ARROW_UP        |             |
NUM_ONE        |             |
NUM_TWO       |             |
NUM_THREE      |             |
NUM_ENTER     |             |
LEFT_CONTROL     |             |
LEFT_WINDOWS       |             |
LEFT_ALT      |             |
SPACE       |             |
RIGHT_ALT        |             |
RIGHT_WINDOWS       |             |
APPLICATION_SELECT        |             |
RIGHT_CONTROL        |             |
ARROW_LEFT       |             |
ARROW_DOWN      |             |
ARROW_RIGHT     |             |
NUM_ZERO     |             |
NUM_PERIOD       |             |
