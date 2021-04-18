---
description: Die Kategorie "Sensor \_ Kategorie \_ mechanisch" enthält Sensoren, die Informationen im Zusammenhang mit mechanischen Geräten und Messungen bereitstellen.
ms.assetid: d1243303-d26c-45ce-b97b-d554daeeb462
title: SENSOR_CATEGORY_MECHANICAL (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2446559820141b65a70bc75d25680da79563388c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347131"
---
# <a name="sensor_category_mechanical"></a>Sensor \_ Kategorie \_ mechanisch

Die Kategorie "Sensor \_ Kategorie \_ mechanisch" enthält Sensoren, die Informationen im Zusammenhang mit mechanischen Geräten und Messungen bereitstellen.

**Platt Form definierte Sensor Typen**

Diese Kategorie enthält die folgenden Platt Form definierten Sensortypen.



| Sensortyp                                                                                                                                                                                                                                                                                                           | BESCHREIBUNG                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------|
| <span id="SENSOR_TYPE_BOOLEAN_SWITCH"></span><span id="sensor_type_boolean_switch"></span><dl> <dt>**Sensor \_ Geben Sie den \_ booleschen \_ Switch**</dt> <dt>{9c7e371f -1041-460b-8d5c-71e4752e350 c}</dt> ein. </dl>                    | Zwei-Status-Switches (Off oder on).<br/>          |
| <span id="SENSOR_TYPE_BOOLEAN_SWITCH_ARRAY"></span><span id="sensor_type_boolean_switch_array"></span><dl> <dt>**Sensor \_ Geben Sie ein \_ Boolesches \_ Switch- \_ Array**</dt> <dt>{545c8ba5-b143-4545-868f-ca7td986b4f</dt> </dl> | Array von Switches mit zwei Zuständen (Off oder on).<br/> |
| <span id="SENSOR_TYPE_FORCE"></span><span id="sensor_type_force"></span><dl> <dt>**Sensor \_ Type \_ Force**</dt> <dt>{C2AB2B02-1a1c-4778-A81B-954a1788cc75}</dt> </dl>                                                | Erzwingen von Sensoren.<br/>                           |
| <span id="SENSOR_TYPE_MULTIVALUE_SWITCH"></span><span id="sensor_type_multivalue_switch"></span><dl> <dt>**Sensor \_ Geben Sie \_ einen mehrwertigen \_ Switch**</dt> ein <dt>{B3EE4D76-37A4-4402-B25E-99C60A775FA1}</dt> . </dl>           | Schalter mit mehreren Positionen.<br/>              |
| <span id="SENSOR_TYPE_PRESSURE"></span><span id="sensor_type_pressure"></span><dl> <dt>**Sensor \_ \_Typdruck**</dt> <dt>{26d31f34-6352-41cf-b793-ea0713d53d77}</dt> </dl>                                       | Drucksensoren.<br/>                        |
| <span id="SENSOR_TYPE_SCALE"></span><span id="sensor_type_scale"></span><dl> <dt>**Sensor \_ \_Typskala**</dt> <dt>{C06DD92C-7FEB-438E-9BF6-82207FFF5BB8}</dt> </dl>                                                | Gewichtungs Sensoren.<br/>                          |
| <span id="SENSOR_TYPE_STRAIN"></span><span id="sensor_type_strain"></span><dl> <dt>**Sensor \_ \_Typbelastung**</dt> <dt>{C6D1EC0E-6803-4361-AD3D-85bcc58c6d29}</dt> </dl>                                             | Belastungssensoren.<br/>                          |



**Platt Form definierte Datenfelder**

Platt Form definierte Eigenschafts Schlüssel für diese Kategorie basieren auf dem \_ Sensor \_ Datentyp \_ GUID- \_ \_ GUID:

{38564a7c-f2f2-49bb-9b2b-ba60f66a58df}

Diese Kategorie enthält die folgenden Platt Form definierten Datenfelder.



| Name und PID des Daten Felds                                                                                                                                                                                                                                                                                                         | BESCHREIBUNG                                                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ABSOLUTE_PRESSURE_PASCAL"></span><span id="sensor_data_type_absolute_pressure_pascal"></span><dl> <dt>**Sensor \_ \_Datentyp \_ absoluter \_ Druck \_ Pascal**</dt> <dt> (PID = 5)</dt> </dl>          | **VT \_ R8**<br/> Absoluter Druck in Pascals.<br/>                    |
| <span id="SENSOR_DATA_TYPE_BOOLEAN_SWITCH_ARRAY_STATES"></span><span id="sensor_data_type_boolean_switch_array_states"></span><dl> <dt>**Sensor \_ \_ \_ Boolesche Switch- \_ \_ array \_ Zustände des Datentyps**</dt> <dt>(PID = 10)</dt> </dl> | **VT \_ UI4**<br/> Zustands Felder für ein Array von booleschen Switches.<br/>   |
| <span id="SENSOR_DATA_TYPE_BOOLEAN_SWITCH_STATE"></span><span id="sensor_data_type_boolean_switch_state"></span><dl> <dt>**Sensor \_ \_ \_ Boolescher Switch- \_ \_ Status des Datentyps**</dt> <dt>(PID = 2)</dt> </dl>                       | **VT \_ bool**<br/> Status Feld für den \_ \_ booleschen Sensortyp- \_ Switch.<br/>  |
| <span id="SENSOR_DATA_TYPE_FORCE_NEWTONS"></span><span id="sensor_data_type_force_newtons"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Force \_ Newtons**</dt> <dt> (PID = 4)</dt> </dl>                                            | **VT \_ R8**<br/> Force in Newtons.<br/>                                |
| <span id="SENSOR_DATA_TYPE_GAUGE_PRESSURE_PASCAL"></span><span id="sensor_data_type_gauge_pressure_pascal"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Mess \_ Gerät Druck \_ Pascal**</dt> <dt> (PID = 6)</dt> </dl>                   | **VT \_ R8**<br/> Relativer Mess Gerät Druck in Pascals.<br/>              |
| <span id="SENSOR_DATA_TYPE_MULTIVALUE_SWITCH_STATE"></span><span id="sensor_data_type_multivalue_switch_state"></span><dl> <dt>**Sensor \_ Datentyp: \_ \_ mehr wertiger \_ Wechsel \_ Status**</dt> <dt> (PID = 3)</dt> </dl>             | **VT \_ R8**<br/> Status Feld für den \_ mehrwertigen Sensortyp- \_ \_ Switch.<br/> |
| <span id="SENSOR_DATA_TYPE_STRAIN"></span><span id="sensor_data_type_strain"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Belastung**</dt> <dt> (PID = 7)</dt> </dl>                                                                  | **VT \_ R8**<br/> Pazi.<br/>                                           |
| <span id="SENSOR_DATA_TYPE_WEIGHT_KILOGRAMS"></span><span id="sensor_data_type_weight_kilograms"></span><dl> <dt>**Sensor \_ \_Gewichtung des \_ \_ Datentyps**</dt> <dt> (PID = 8)</dt> </dl>                                   | **VT \_ R8**<br/> Gewichtung in Kilogramm.<br/>                             |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensoren. h</dt> </dl> |



 

 




