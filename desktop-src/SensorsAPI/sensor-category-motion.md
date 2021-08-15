---
description: Die Kategorie SENSOR CATEGORY MOTION enthält Sensoren, die Informationen im Zusammenhang \_ mit der \_ physischen Bewegung bereitstellen.
ms.assetid: be025c86-46b5-4f50-a3af-0408bb3c9b5b
title: SENSOR_CATEGORY_MOTION (Sensors.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a66d57c8406ad1344d696f63e574484943ea68a6654f63c3d7d38e904aaa44e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889488"
---
# <a name="sensor_category_motion"></a>\_ \_ SENSORKATEGORIEBEWEGUNG

Die Kategorie SENSOR CATEGORY MOTION enthält Sensoren, die Informationen im Zusammenhang \_ mit der \_ physischen Bewegung bereitstellen. Beschleunigungsmesser messen die Beschleunigung des Sensors, einschließlich der beschleunigungsbeschleunigung. Bewegungserkennungen, z. B. die Erkennung menschlicher Bewegungen in einem Sicherheitssystem, erkennen bewegte Objekte. Gyrometer sehen Änderungen der Winkelgeschwindigkeit. Geschwindigkeitsmesser messen die Geschwindigkeit.

**Plattformdefinierte Sensortypen**

Diese Kategorie umfasst die folgenden plattformdefinierten Sensortypen.



| Sensortyp                                                                                                                                                                                                                                                                                              | BESCHREIBUNG                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="SENSOR_TYPE_ACCELEROMETER_1D"></span><span id="sensor_type_accelerometer_1d"></span><dl> <dt>**SENSOR \_ GEBEN \_ SIE ACCELEROMETER \_ 1D**</dt> <dt>{C04D2387-7340-4CC2-991E-3B18CB8EF2F4} EIN.</dt> </dl> | Beschleunigungsmesser mit einer Achse.<br/>                                  |
| <span id="SENSOR_TYPE_ACCELEROMETER_2D"></span><span id="sensor_type_accelerometer_2d"></span><dl> <dt>**SENSOR \_ GEBEN \_ SIE ACCELEROMETER \_ 2D**</dt> <dt>{B2C517A8-F6B5-4BA6-A423-5DF560B4CC07} EIN.</dt> </dl> | Beschleunigungsmesser mit zwei Achsen.<br/>                                  |
| <span id="SENSOR_TYPE_ACCELEROMETER_3D"></span><span id="sensor_type_accelerometer_3d"></span><dl> <dt>**SENSOR \_ GEBEN \_ SIE ACCELEROMETER \_ 3D**</dt> <dt>{C2FB0F5F-E2D2-4C78-BCD0-352A9582819D} EIN.</dt> </dl> | Beschleunigungsmesser mit drei Achsen.<br/>                                |
| <span id="SENSOR_TYPE_GYROMETER_1D"></span><span id="sensor_type_gyrometer_1d"></span><dl> <dt>**SENSOR \_ TYP \_ GYROMETER \_ 1D**</dt> <dt>{FA088734-F552-4584-8324-AF649652C}</dt> </dl>             | Einachsen-Gyrometer.<br/>                                      |
| <span id="SENSOR_TYPE_GYROMETER_2D"></span><span id="sensor_type_gyrometer_2d"></span><dl> <dt>**SENSOR \_ TYP \_ GYROMETER \_ 2D**</dt> <dt>{31EF4F83-919B-48BF-8DE0-5D7A9D240556}</dt> </dl>             | Gyrometer mit zwei Achsen.<br/>                                      |
| <span id="SENSOR_TYPE_GYROMETER_3D"></span><span id="sensor_type_gyrometer_3d"></span><dl> <dt>**SENSOR \_ TYP \_ GYROMETER \_ 3D**</dt> <dt>{09485F5A-759E-42C2-BD4B-A349B75C8643}</dt> </dl>             | Gyrometer mit drei Achsen.<br/>                                    |
| <span id="SENSOR_TYPE_MOTION_DETECTOR"></span><span id="sensor_type_motion_detector"></span><dl> <dt>**SENSOR \_ TYPE \_ MOTION \_ DETECTOR**</dt> <dt>{5C7C1A12-30A5-43B9-A4B2-CF09EC5B7BE8}</dt> </dl>    | Bewegungserkennungen, z. B. solche, die in Sicherheitssystemen verwendet werden.<br/> |
| <span id="SENSOR_TYPE_SPEEDOMETER"></span><span id="sensor_type_speedometer"></span><dl> <dt>**SENSOR \_ TYPE \_ SPEEDOMETER**</dt> <dt>{6BD73C1F-0BB4-4310-81B2-DFC18A52BF94}</dt> </dl>                 | Bewegungsratensensoren.<br/>                                   |



**Plattformdefinierte Datenfelder**

Plattformdefinierte Eigenschaftsschlüssel für diese Kategorie basieren auf SENSOR \_ DATA \_ TYPE MOTION \_ \_ GUID:

{3F8A69A2-07C5-4E48-A965-CD797AAB56D5}

Diese Kategorie umfasst die folgenden plattformdefinierten Datenfelder.



| Datenfeldname und PID                                                                                                                                                                                                                                                                                                                                                                               | BESCHREIBUNG                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ACCELERATION_X_G"></span><span id="sensor_data_type_acceleration_x_g"></span><dl> <dt>**SENSOR \_ \_ \_ DATENTYPBESCHLEUNIGUNG \_ X \_ G**</dt> <dt>(PID = 2)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Beschleunigung der X-Achse in *g*' s.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ACCELERATION_Y_G"></span><span id="sensor_data_type_acceleration_y_g"></span><dl> <dt>**SENSOR \_ \_ \_ DATENTYPBESCHLEUNIGUNG \_ Y \_ G**</dt> <dt>(PID = 3)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Beschleunigung der Y-Achse in *g*'s.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ACCELERATION_Z_G"></span><span id="sensor_data_type_acceleration_z_g"></span><dl> <dt>**SENSOR \_ \_ \_ DATENTYPBESCHLEUNIGUNG \_ Z \_ G**</dt> <dt>(PID = 4)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Beschleunigung der Z-Achse in *g*' s.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_X_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_x_degrees_per_second_squared"></span><dl> <dt>**SENSOR \_ DATENTYP \_ \_ ANGULAR \_ ACCELERATION X \_ \_ DEGREES PER SECOND \_ \_ \_ SQUARED**</dt> <dt>(PID = 5)</dt> </dl>  | **VT \_ R8**<br/> Gyrometrische X-Achsenbeschleunigung in Grad pro Sekunde quadratisch.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_Y_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_y_degrees_per_second_squared"></span><dl> <dt>**SENSOR \_ DATENTYP \_ \_ ANGULAR \_ ACCELERATION \_ Y \_ DEGREES PER SECOND \_ \_ \_ SQUARED**</dt> <dt> (PID = 6)</dt> </dl> | **VT \_ R8**<br/> Gyrometrische Beschleunigung der y-Achse in Grad pro Sekunde quadratisch.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_Z_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_z_degrees_per_second_squared"></span><dl> <dt>**SENSOR \_ DATENTYP \_ \_ ANGULAR \_ ACCELERATION Z \_ \_ DEGREES PER SECOND \_ \_ \_ SQUARED**</dt> <dt> (PID = 7)</dt> </dl> | **VT \_ R8**<br/> Gyrometrische Z-Achsenbeschleunigung in Grad pro Sekunde quadratisch.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_X_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_x_degrees_per_second"></span><dl> <dt>**SENSOR \_ DATENTYP \_ \_ ANGULARGESCHWINDIGKEIT \_ X GRAD PRO \_ \_ \_ \_ SEKUNDE**</dt> <dt> (PID = 10)</dt> </dl>                                      | **VT \_ R8**<br/> Gyrometrische X-Achsengeschwindigkeit in Grad pro Sekunde.<br/>             |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_Y_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_y_degrees_per_second"></span><dl> <dt>**SENSOR \_ DATENTYP \_ \_ ANGULARGESCHWINDIGKEIT \_ \_ Y \_ GRAD PRO \_ \_ SEKUNDE**</dt> <dt> (PID = 11)</dt> </dl>                                      | **VT \_ R8**<br/> Gyrometrische y-Achsengeschwindigkeit in Grad pro Sekunde.<br/>             |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_Z_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_z_degrees_per_second"></span><dl> <dt>**SENSOR \_ DATENTYP \_ \_ ANGULARGESCHWINDIGKEIT \_ Z GRAD PRO \_ \_ \_ \_ SEKUNDE**</dt> <dt> (PID = 12)</dt> </dl>                                      | **VT \_ R8**<br/> Gyrometrische Z-Achsengeschwindigkeit in Grad pro Sekunde.<br/>             |
| <span id="SENSOR_DATA_TYPE_MOTION_STATE"></span><span id="sensor_data_type_motion_state"></span><dl> <dt>**SENSOR \_ DATENTYP \_ MOTION \_ \_ STATE**</dt> <dt>(PID = 9)</dt> </dl>                                                                                                                      | **VT \_ BOOL**<br/> **TRUE,** wenn Bewegung erkannt wird; andernfalls **FALSE**.<br/>        |
| <span id="SENSOR_DATA_TYPE_SPEED_METERS_PER_SECOND"></span><span id="sensor_data_type_speed_meters_per_second"></span><dl> <dt>**SENSOR \_ DATENTYP \_ \_ \_ GESCHWINDIGKEITSZÄHLER \_ PRO \_ SEKUNDE**</dt> <dt> (PID = 8)</dt> </dl>                                                                                  | **VT \_ R8**<br/> Geschwindigkeit in Metern pro Sekunde.<br/>                                    |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensors.h</dt> </dl> |



 

 




