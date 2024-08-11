---
제목 : "Tuya TS0601_dimmer_5 control by MQTT"
설명: "Zigbee2를 통해 Tuya TS0601_dimmer_5를 통합하십시오.공급업체의 브리지나 게이트웨이 없이 사용 중인 모든 스마트 홈 인프라를 갖춘 MQTT."
추가일자 : 2023-11-30T19:41:12
pageClass: device-page
---

<!-- !!!! -->
<!-- ATTENTION: This file is auto-generated through docgen! -->
<!-- You can only edit the "Notes"-Section between the two comment lines "Notes BEGIN" and "Notes END". -->
<!-- Do not use h1 or h2 heading within "## Notes"-Section. -->
<!-- !!!! -->

# Tuya TS0601_dimmer_5![Tuya TS0601_dimmer_5]


|     |     |
|-----|-----|
| Model | TS0601_dimmer_5  |
| Vendor  | [Tuya](/supported-devices/#v=Tuya)  |
| Description | 1 gang smart dimmer module |
| Exposes | light (state, brightness, min_brightness, max_brightness), power_on_behavior, countdown, light_type, switch_type, linkquality |
| Picture | ![Tuya TS0601_dimmer_5](https://github.com/user-attachments/assets/6f1d7b0c-5ab0-4146-adb3-52133db4bc9b) |
| White-label | Moes MS-105-M |


<!-- Notes BEGIN: You can edit here. Add "## Notes" headline if not already present. -->


<!-- Notes END: Do not edit below this line -->




## Exposes

### Light 
This light supports the following features: `state`, `brightness`, `min_brightness`, `max_brightness`.
- `state`: To control the state publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"state": "ON"}`, `{"state": "OFF"}` or `{"state": "TOGGLE"}`. To read the state send a message to `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"state": ""}`.
- `brightness`: To control the brightness publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"brightness": VALUE}` where `VALUE` is a number between `0` and `254`. To read the brightness send a message to `zigbee2mqtt/FRIENDLY_NAME/get` with payload `{"brightness": ""}`.

### Power on behavior (enum)
Value can be found in the published state on the `power_on_behavior` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"power_on_behavior": NEW_VALUE}`.
The possible values are: `off`, `on`, `previous`.

### Countdown (numeric)
Countdown to turn device off after a certain time.
Value can be found in the published state on the `countdown` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"countdown": NEW_VALUE}`.
The minimal value is `0` and the maximum value is `43200`.
The unit of this value is `s`.

### Light type (enum)
Type of light attached to the device.
Value can be found in the published state on the `light_type` property.
It's not possible to read (`/get`) this value.
To write (`/set`) a value publish a message to topic `zigbee2mqtt/FRIENDLY_NAME/set` with payload `{"light_type": NEW_VALUE}`.
The possible values are: `led`, `incandescent`, `halogen`.

### Switch type (enum)
Type of the switch.
Value can be found in the published state on the `switch_type` property.
To read (`/겟`) the value publish a message to topic `지그비2mqtt/FRIENDY_NAME/get` with payload `{"switch_type": ""}`.
값을 작성하려면('/set') "{"switch_type": NEW_VALUE}" 페이로드로 "zigbee2mqtt/FRIEND_NAME/set" 토픽에 메시지를 게시합니다.
The possible values are: `토글`, `주`, `순간적으로`.

### 링크품질(숫자)
링크 품질(신호 강도).
가치는 '링크 품질' 속성에 대한 게시 상태에서 찾을 수 있습니다.
이 값을 읽거나('/get') 쓸 수 없습니다('/set').
최소값은 '0'이고 최대값은 '255'입니다.
이 값의 단위는 'lqi'입니다.

