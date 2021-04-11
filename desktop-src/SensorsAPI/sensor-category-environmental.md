---
description: Die \_ Kategorie Kategorie "Kategorie" \_ enthält Sensoren, die Informationen zur umgebenden Umgebung oder zum Wetter bereitstellen.
ms.assetid: 4a29d44b-8949-474d-a2bf-0c6e1d30b198
title: SENSOR_CATEGORY_ENVIRONMENTAL (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b5c41d4c117dc27a3303210a485b2233cf24cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862264"
---
# <a name="sensor_category_environmental"></a>Sensor \_ Kategorie \_ Umwelt

Die \_ Kategorie Kategorie "Kategorie" \_ enthält Sensoren, die Informationen zur umgebenden Umgebung oder zum Wetter bereitstellen.

**Platt Form definierte Sensor Typen**

Diese Kategorie enthält die folgenden Platt Form definierten Sensortypen.



| Sensortyp                                                                                                                                                                                                                                                                                                                                                     | BESCHREIBUNG               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------|
| <span id="SENSOR_TYPE_ENVIRONMENTAL_ATMOSPHERIC_PRESSURE"></span><span id="sensor_type_environmental_atmospheric_pressure"></span><dl> <dt>**Sensor \_ Geben Sie \_ Environmental \_ ATMOSPHERIC \_ Pressure**</dt> <dt>{0e903829-ff8a-4A93-97df-3dcbde402288}</dt> ein. </dl> | Barometer.<br/>    |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_HUMIDITY"></span><span id="sensor_type_environmental_humidity"></span><dl> <dt>**Sensor \_ Geben Sie \_ Environmental \_ Feuchtigkeit**</dt> <dt>{5c72bf 67-bd7e-4257-990b-98a3ba3b400a} ein</dt> . </dl>                                      | Bindestriche.<br/>   |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_TEMPERATURE"></span><span id="sensor_type_environmental_temperature"></span><dl> <dt>**Sensor \_ Geben Sie \_ Environmental \_ Temperatur**</dt> <dt>{04fd0ec4-d5da-45fa-95a9-5db38ee19306} ein.</dt> </dl>                             | Thermometer<br/>   |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_WIND_DIRECTION"></span><span id="sensor_type_environmental_wind_direction"></span><dl> <dt>**Sensor \_ Geben Sie " \_ Environmental \_ Wind \_ Direction**</dt> <dt>{9ef57a35-9306-434d-af09-37fa5a9c00bd}</dt> " ein. </dl>                   | Wetter-Vanes.<br/> |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_WIND_SPEED"></span><span id="sensor_type_environmental_wind_speed"></span><dl> <dt>**Sensor \_ Geben Sie " \_ Umwelt \_ Wind \_ Geschwindigkeit**</dt> <dt>{DD50607B-A45F-42CD-8EFD-EC61761C4226}</dt> " ein. </dl>                               | Anemometer.<br/>   |



**Platt Form definierte Datenfelder**

Platt Form definierte Eigenschafts Schlüssel für diese Kategorie basieren auf dem Sensor- \_ \_ Datentyp \_ Umwelt- \_ GUID:

{8b0aa2o1-2 D57-42ee-8cc0-4d27622b46c4}

Diese Kategorie enthält die folgenden Platt Form definierten Datenfelder.



| Name und PID des Daten Felds                                                                                                                                                                                                                                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ATMOSPHERIC_PRESSURE_BAR"></span><span id="sensor_data_type_atmospheric_pressure_bar"></span><dl> <dt>**Sensor \_ Der \_ Datentyp " \_ atmosphärische \_ Druck \_ Leiste**</dt> " <dt>(PID = 4)</dt> </dl>                                      | **VT \_ R4**<br/> Der atmosphärische Druck in den Atmosphären (Balken).<br/>                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_TEMPERATURE_CELSIUS"></span><span id="sensor_data_type_temperature_celsius"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Temperatur \_ Celsius**</dt> <dt>(PID = 2)</dt> </dl>                                                      | **VT \_ R4**<br/> Temperatur in Grad Celsius.<br/>                                                                                                                                                          |
| <span id="SENSOR_DATA_TYPE_RELATIVE_HUMIDITY_PERCENT"></span><span id="sensor_data_type_relative_humidity_percent"></span><dl> <dt>**Sensor \_ \_Datentyp \_ relative \_ Luftfeuchtigkeit \_ %**</dt> <dt> (PID = 3)</dt> </dl>                                  | **VT \_ R4**<br/> Relative Luftfeuchtigkeit als Prozentsatz.<br/>                                                                                                                                                       |
| <span id="SENSOR_DATA_TYPE_WIND_DIRECTION_DEGREES_ANTICLOCKWISE"></span><span id="sensor_data_type_wind_direction_degrees_anticlockwise"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Wind \_ Richtung \_ \_ gegen den Uhrzeigersinn**</dt> <dt>(PID = 5)</dt> </dl> | **VT \_ R4**<br/> Wind Richtung relativ zum Magnet Nord in Grad. North wird als 0,0 (oben auf der X-Achse) dargestellt, wobei sich die Werte in der Drehung gegen den Uhrzeigersinn erhöhen. Die Z-Achse zeigt nach oben. <br/> |
| <span id="SENSOR_DATA_TYPE_WIND_SPEED_METERS_PER_SECOND"></span><span id="sensor_data_type_wind_speed_meters_per_second"></span><dl> <dt>**Sensor \_ \_Datentyp \_ \_ Windgeschwindigkeits- \_ Zähler \_ pro \_ Sekunde**</dt> <dt>(PID = 6)</dt> </dl>                        | **VT \_ R4**<br/> Wind Geschwindigkeit in Meter pro Sekunde.<br/>                                                                                                                                                         |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensoren. h</dt> </dl> |



 

 




