---
title: "Zemismart M515EGBZTN control via MQTT"
description: "Integrate your Zemismart M515EGBZTN via Zigbee2MQTT with whatever smart home infrastructure you are using without the vendor's bridge or gateway."
addedAt: 2022-08-31T11:26:27
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# Zemismart M515EGBZTN

|     |     |
|-----|-----|
| Model | M515EGBZTN  |
| Vendor  | [Zemismart](/supported-devices/#v=Zemismart)  |
| Description | Roller shade driver |
| Exposes | cover (state, position), motor_direction, border, linkquality |
| Picture | ![Zemismart M515EGBZTN](https://www.zigbee2mqtt.io/images/devices/M515EGBZTN.jpg) |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->

## Notes
Important note for those who have the second generation device (labeled as TM616EGBZTN but recognized as M515EGBZTN in Zigbee2MQTT): 
The official documentation states only provides instructions on how to set the limits via app (via Z2M ui using the Z2M integration).
But there's undocumented way to set the limits also on the device (as it is also possible with the older / first generation M515EGBZTN devices which are also identified as M515EGBZTN in Z2M). To set limits using the buttons on the device do the following:
1. Press and hold 'Up' & 'Down' button at the same time for about 5 seconds.
2. The device will shortly flash red and then it will blink continously with blue color.
3. Now go to the first limit position (if in 'forward' mode which is the factory setting this is the upper limit). Once reached press the 'Stop' button twice very quickly -> first limit is set.
4. Now go to the second limit position (if in 'forward' mode which is the factory setting this is the lower limit). Once reached press the 'Stop' button again twice very quickly -> second limit is set.
<!-- Notes END: Do not edit below this line -->



## Options
*[How to use device type specific configuration](../guide/configuration/devices-groups.md#specific-device-options)*

* `invert_cover`: Inverts the cover position, false: open=100,close=0, true: open=0,close=100 (default false). The value must be `true` or `false`


## Exposes

### Cover 
The current state of this cover is in the published state under the `state` property (value is `OPEN` or `CLOSE`).
To control this cover publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"state": "OPEN"}`, `{"state": "CLOSE"}`, `{"state": "STOP"}`.
It's not possible to read (`/get`) this value.
To change the position publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"position": VALUE}` where `VALUE` is a number between `0` and `100`.

### Motor direction (enum)
Value can be found in the published state on the `motor_direction` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"motor_direction": NEW_VALUE}`.
The possible values are: `forward`, `back`.

### Border (enum)
Value can be found in the published state on the `border` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"border": NEW_VALUE}`.
The possible values are: `up`, `down`, `down_delete`.

### Linkquality (numeric)
Link quality (signal strength).
Value can be found in the published state on the `linkquality` property.
It's not possible to read (`/get`) or write (`/set`) this value.
The minimal value is `0` and the maximum value is `255`.
The unit of this value is `lqi`.

