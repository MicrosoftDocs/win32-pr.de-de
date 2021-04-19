---
description: Die Motion-Kategorie der Sensor \_ Kategorie \_ enthält Sensoren, die Informationen im Zusammenhang mit physischer Bewegung bereitstellen.
ms.assetid: be025c86-46b5-4f50-a3af-0408bb3c9b5b
title: SENSOR_CATEGORY_MOTION (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1edcb1b5f0a6d02c481774d18ee111ad4ca5e5cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348368"
---
# <a name="sensor_category_motion"></a>Motion der Sensor \_ Kategorie \_

Die Motion-Kategorie der Sensor \_ Kategorie \_ enthält Sensoren, die Informationen im Zusammenhang mit physischer Bewegung bereitstellen. Beschleunigungsmesser messen die Beschleunigung des Sensors, einschließlich der Gravitationsbeschleunigung. Bewegungsmelder, wie z. b. die Erkennung von Menschen Bewegungen in einem Sicherheitssystem, sind das Verschieben von Objekten. "Gyrometer Sense" ändert sich in der Winkelgeschwindigkeit. Geschwindigkeitsmessung der Geschwindigkeit.

**Platt Form definierte Sensor Typen**

Diese Kategorie enthält die folgenden Platt Form definierten Sensortypen.



| Sensortyp                                                                                                                                                                                                                                                                                              | BESCHREIBUNG                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="SENSOR_TYPE_ACCELEROMETER_1D"></span><span id="sensor_type_accelerometer_1d"></span><dl> <dt>**Sensor \_ Type \_ Accelerometer \_ 1D**</dt> <dt>{C04D2387-7340-4CC2-991E-3B18CB8EF2F4}</dt> </dl> | One-Achse-Beschleunigungsmesser.<br/>                                  |
| <span id="SENSOR_TYPE_ACCELEROMETER_2D"></span><span id="sensor_type_accelerometer_2d"></span><dl> <dt>**Sensor \_ Type \_ Accelerometer \_ 2D**</dt> <dt>{B2C517A8-F6B5-4BA6-A423-5DF560B4CC07}</dt> </dl> | 2-Achsen-Beschleunigungsmesser.<br/>                                  |
| <span id="SENSOR_TYPE_ACCELEROMETER_3D"></span><span id="sensor_type_accelerometer_3d"></span><dl> <dt>**Sensor \_ Type \_ Accelerometer \_ 3D**</dt> <dt>{C2FB0F5F-E2D2-4C78-BCD0-352A9582819D}</dt> </dl> | Drei-Achsen-Beschleunigungsmesser.<br/>                                |
| <span id="SENSOR_TYPE_GYROMETER_1D"></span><span id="sensor_type_gyrometer_1d"></span><dl> <dt>**Sensor \_ \_Typgyrometer \_ 1D**</dt> <dt>{FA088734-F552-4584-8324-EDFAF649652C}</dt> </dl>             | Gyrometer mit einer Achse.<br/>                                      |
| <span id="SENSOR_TYPE_GYROMETER_2D"></span><span id="sensor_type_gyrometer_2d"></span><dl> <dt>**Sensor \_ Geben Sie " \_ Gyrometer \_ 2D**</dt> <dt>{31ef4f 83-919b-48bf -8de0-5d7a9d240556}</dt> " ein. </dl>             | Gyrometer mit zwei Achsen.<br/>                                      |
| <span id="SENSOR_TYPE_GYROMETER_3D"></span><span id="sensor_type_gyrometer_3d"></span><dl> <dt>**Sensor \_ Geben Sie " \_ Gyrometer \_ 3D**</dt> <dt>{09485b-759e-42C2-BD4B-a349b75c8643}</dt> " ein. </dl>             | Drei-Achsen-Gyrometer.<br/>                                    |
| <span id="SENSOR_TYPE_MOTION_DETECTOR"></span><span id="sensor_type_motion_detector"></span><dl> <dt>**Sensor \_ Type \_ Motion \_ Detector**</dt> <dt>{5c7c1a12-30a5-43b9-a4b2-cf09ec5b7be8}</dt> </dl>    | Bewegungsmelder, z. b. solche, die in Sicherheitssystemen verwendet werden.<br/> |
| <span id="SENSOR_TYPE_SPEEDOMETER"></span><span id="sensor_type_speedometer"></span><dl> <dt>**Sensor \_ Geben Sie " \_ speedometer**</dt> <dt>{6bd73c1f-0bb4-4310-81b2-dfc18a52bf94}</dt> " ein. </dl>                 | Rate der Bewegungssensoren.<br/>                                   |



**Platt Form definierte Datenfelder**

Platt Form definierte Eigenschafts Schlüssel für diese Kategorie basieren auf dem Sensor- \_ \_ Datentyp \_ Motion \_ GUID:

{3F 8a69a2-07c5-4e48-A965-cd797aab56d5}

Diese Kategorie enthält die folgenden Platt Form definierten Datenfelder.



| Name und PID des Daten Felds                                                                                                                                                                                                                                                                                                                                                                               | BESCHREIBUNG                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ACCELERATION_X_G"></span><span id="sensor_data_type_acceleration_x_g"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Beschleunigung \_ X \_ G**</dt> <dt>(PID = 2)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Beschleunigung der X-Achse in *g*.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ACCELERATION_Y_G"></span><span id="sensor_data_type_acceleration_y_g"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Beschleunigung \_ Y \_ G**</dt> <dt>(PID = 3)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Beschleunigung der Y-Achse in *g*.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ACCELERATION_Z_G"></span><span id="sensor_data_type_acceleration_z_g"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Beschleunigung \_ Z \_ G**</dt> <dt>(PID = 4)</dt> </dl>                                                                                                         | **VT \_ R8**<br/> Beschleunigung der Z-Achse in *g*.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_X_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_x_degrees_per_second_squared"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Angular \_ Acceleration \_ X \_ Grad \_ pro \_ Sekunde \_ quadratisch**</dt> <dt>(PID = 5)</dt> </dl>  | **VT \_ R8**<br/> Beschleunigung der x-Achse der gyrometrik, in Grad pro Sekunde (quadratisch).<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_Y_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_y_degrees_per_second_squared"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Winkel \_ Beschleunigung \_ Y \_ Grad \_ pro \_ Sekunde \_ quadriert**</dt> <dt> (PID = 6)</dt> </dl> | **VT \_ R8**<br/> Beschleunigung der y-Achse der gyrometrik (in Grad pro Sekunde, Quadrat).<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_Z_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_z_degrees_per_second_squared"></span><dl> <dt>**Sensor \_ Data \_ Type \_ Angular \_ Acceleration \_ Z \_ Grad \_ pro \_ Sekunde \_ quadriert**</dt> <dt> (PID = 7)</dt> </dl> | **VT \_ R8**<br/> Der gyrometric-z-Achsen-Beschleunigung in Grad pro Sekunde in Quadrat.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_X_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_x_degrees_per_second"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Angular- \_ Geschwindigkeit \_ X \_ Grad \_ pro \_ Sekunde**</dt> <dt> (PID = 10)</dt> </dl>                                      | **VT \_ R8**<br/> Geschwindigkeit der x-Achse der gyrometrik (in Grad pro Sekunde).<br/>             |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_Y_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_y_degrees_per_second"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Winkel \_ Geschwindigkeit \_ Y \_ Grad \_ pro \_ Sekunde**</dt> <dt> (PID = 11)</dt> </dl>                                      | **VT \_ R8**<br/> Die Geschwindigkeit der y-Achse der gyrometrik (in Grad pro Sekunde).<br/>             |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_Z_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_z_degrees_per_second"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Angular \_ Velocity \_ Z \_ Grad \_ pro \_ Sekunde**</dt> <dt> (PID = 12)</dt> </dl>                                      | **VT \_ R8**<br/> Gyrometric-z-Achsen-Geschwindigkeit in Grad pro Sekunde.<br/>             |
| <span id="SENSOR_DATA_TYPE_MOTION_STATE"></span><span id="sensor_data_type_motion_state"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Motion \_ State**</dt> <dt>(PID = 9)</dt> </dl>                                                                                                                      | **VT \_ bool**<br/> **True** , wenn Bewegung erkannt wird. andernfalls **false**.<br/>        |
| <span id="SENSOR_DATA_TYPE_SPEED_METERS_PER_SECOND"></span><span id="sensor_data_type_speed_meters_per_second"></span><dl> <dt>**Sensor \_ Datentyp- \_ \_ Geschwindigkeits \_ Zähler \_ pro \_ Sekunde**</dt> <dt> (PID = 8)</dt> </dl>                                                                                  | **VT \_ R8**<br/> Geschwindigkeit in Meter pro Sekunde.<br/>                                    |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensoren. h</dt> </dl> |



 

 




