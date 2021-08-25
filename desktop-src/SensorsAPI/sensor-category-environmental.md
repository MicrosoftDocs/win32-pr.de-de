---
description: Die Kategorie SENSOR \_ CATEGORY \_ ENVIRONMENTAL enthält Sensoren, die Informationen zur umgebungs- oder wetterbedingten Umgebung bereitstellen.
ms.assetid: 4a29d44b-8949-474d-a2bf-0c6e1d30b198
title: SENSOR_CATEGORY_ENVIRONMENTAL (Sensors.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7cc2a6ca1d2832045a77f0a2ffa1902732e484700afaacd757719e99d667c55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126610"
---
# <a name="sensor_category_environmental"></a>UMGEBUNG \_ DER \_ SENSORKATEGORIE

Die Kategorie SENSOR \_ CATEGORY \_ ENVIRONMENTAL enthält Sensoren, die Informationen zur umgebungs- oder wetterbedingten Umgebung bereitstellen.

**Plattformdefinierte Sensortypen**

Diese Kategorie umfasst die folgenden plattformdefinierten Sensortypen.



| Sensortyp                                                                                                                                                                                                                                                                                                                                                     | Beschreibung               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------|
| <span id="SENSOR_TYPE_ENVIRONMENTAL_ATMOSPHERIC_PRESSURE"></span><span id="sensor_type_environmental_atmospheric_pressure"></span><dl> <dt>**SENSOR \_ TYP \_ ENVIRONMENTAL \_ PRESSURE \_**</dt> <dt>{0E903829-FF8A-4A93-97DF-3DCBDE402288}</dt> </dl> | Barometer.<br/>    |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_HUMIDITY"></span><span id="sensor_type_environmental_humidity"></span><dl> <dt>**SENSOR \_ TYP \_ \_ UMGEBUNGSLUFTFEUCHTIGKEIT**</dt> <dt>{5C72BF67-BD7E-4257-990B-98A3BA3B400A}</dt> </dl>                                      | Hygrometer.<br/>   |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_TEMPERATURE"></span><span id="sensor_type_environmental_temperature"></span><dl> <dt>**SENSOR \_ TYP \_ \_ UMGEBUNGSTEMPERATUR**</dt> <dt>{04FD0EC4-D5DA-45FA-95A9-5DB38EE19306}</dt> </dl>                             | Thermometer<br/>   |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_WIND_DIRECTION"></span><span id="sensor_type_environmental_wind_direction"></span><dl> <dt>**SENSOR \_ TYP \_ ENVIRONMENTAL \_ WIND \_ DIRECTION**</dt> <dt>{9EF57A35-9306-434D-AF09-37FA5A9C00BD}</dt> </dl>                   | Wetter-Vans.<br/> |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_WIND_SPEED"></span><span id="sensor_type_environmental_wind_speed"></span><dl> <dt>**SENSOR \_ TYP \_ \_ \_ UMGEBUNGSWINDGESCHWINDIGKEIT**</dt> <dt>{DD50607B-A45F-42CD-8EFD-EC61761C4226}</dt> </dl>                               | Anemometer.<br/>   |



**Plattformdefinierte Datenfelder**

Plattformdefinierte Eigenschaftsschlüssel für diese Kategorie basieren auf SENSOR \_ DATA \_ TYPE ENVIRONMENTAL \_ \_ GUID:

{8B0AA2F1-2D57-42EE-8CC0-4D27622B46C4}

Diese Kategorie umfasst die folgenden plattformdefinierten Datenfelder.



| Datenfeldname und PID                                                                                                                                                                                                                                                                                                                                    | Beschreibung                                                                                                                                                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ATMOSPHERIC_PRESSURE_BAR"></span><span id="sensor_data_type_atmospheric_pressure_bar"></span><dl> <dt>**SENSOR \_ DATA \_ TYPE PRESSURE PRESSURE \_ \_ \_ BAR**</dt> <dt>(PID = 4)</dt> </dl>                                      | **VT \_ R4**<br/> Druck in Flüssen (Balken).<br/>                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_TEMPERATURE_CELSIUS"></span><span id="sensor_data_type_temperature_celsius"></span><dl> <dt>**SENSOR \_ DATENTYP \_ \_ TEMPERATURE \_ CELSIUS**</dt> <dt>(PID = 2)</dt> </dl>                                                      | **VT \_ R4**<br/> Temperatur in Grad Celsius.<br/>                                                                                                                                                          |
| <span id="SENSOR_DATA_TYPE_RELATIVE_HUMIDITY_PERCENT"></span><span id="sensor_data_type_relative_humidity_percent"></span><dl> <dt>**SENSOR \_ DATENTYP \_ RELATIVE \_ \_ LUFTFEUCHTIGKEIT IN \_ PROZENT**</dt> <dt> (PID = 3)</dt> </dl>                                  | **VT \_ R4**<br/> Relative Luftfeuchtigkeit als Prozentsatz.<br/>                                                                                                                                                       |
| <span id="SENSOR_DATA_TYPE_WIND_DIRECTION_DEGREES_ANTICLOCKWISE"></span><span id="sensor_data_type_wind_direction_degrees_anticlockwise"></span><dl> <dt>**SENSOR \_ DATENTYP \_ \_ \_ WINDRICHTUNG \_ GRAD \_ ANTICLOCKWISE**</dt> <dt>(PID = 5)</dt> </dl> | **VT \_ R4**<br/> Windrichtung relativ zum magnetischen Norden in Grad. North wird als 0,0 (oben auf der X-Achse) dargestellt, und die Werte werden in einer Drehung im Uhrzeigersinn erhöht. Die Z-Achse zeigt nach oben. <br/> |
| <span id="SENSOR_DATA_TYPE_WIND_SPEED_METERS_PER_SECOND"></span><span id="sensor_data_type_wind_speed_meters_per_second"></span><dl> <dt>**SENSOR \_ DATENTYP \_ \_ \_ WINDGESCHWINDIGKEIT METER \_ PRO \_ \_ SEKUNDE**</dt> <dt>(PID = 6)</dt> </dl>                        | **VT \_ R4**<br/> Windgeschwindigkeit in Metern pro Sekunde.<br/>                                                                                                                                                         |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensors.h</dt> </dl> |



 

 




