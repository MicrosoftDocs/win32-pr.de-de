---
description: Die Kategorie "Light" der Sensor \_ Kategorie \_ enthält Sensoren, die Informationen zu den Merkmalen des Lichts bereitstellen.
ms.assetid: 0327bda5-f1d7-476d-9f0f-f4d60a6a106f
title: SENSOR_CATEGORY_LIGHT (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca14bba297a8f445312873fc810e7d0b5ba13a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862263"
---
# <a name="sensor_category_light"></a>Sensor \_ Kategorie \_ hell

Die Kategorie "Light" der Sensor \_ Kategorie \_ enthält Sensoren, die Informationen zu den Merkmalen des Lichts bereitstellen.

**Platt Form definierte Sensor Typen**

Diese Kategorie enthält die folgenden Platt Form definierten Sensortypen.



| Sensortyp                                                                                                                                                                                                                                                                                     | BESCHREIBUNG                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------|
| <span id="SENSOR_TYPE_AMBIENT_LIGHT"></span><span id="sensor_type_ambient_light"></span><dl> <dt>**Sensor \_ Typ \_ AMBIENT \_ Light**</dt> <dt>{97F 115c8-599a-4153-8894-D2D12899918A}</dt> </dl> | Umgebungslichtsensoren.<br/> |



**Platt Form definierte Datenfelder**

Platt Form definierte Eigenschafts Schlüssel für diese Kategorie basieren auf der \_ hell-GUID des Sensor Datentyps \_ \_ \_ :

{E4C77CE2-DCB7-46E9-8439-4FEC548833A6}

Diese Kategorie enthält die folgenden Platt Form definierten Datenfelder.



| Name und PID des Daten Felds                                                                                                                                                                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_LIGHT_CHROMACITY__"></span><span id="sensor_data_type_light_chromacity__"></span><dl> <dt> **Sensor \_ \_ Datentyp \_ Light \_ chromacity**</dt> <dt>(PID = 4)</dt> </dl>                     | **VT \_ Vector \| VT \_ UI1**<br/> Die Chromaticity als Gezähltes Array von float-Werten.<br/> Daten für Vektor Typen werden immer als **VT \_ UI1** (ein Array von Zeichen ohne Vorzeichen, 1 Byte Zeichen) serialisiert. Dieses Datenfeld enthält tatsächlich jeden Wert als einen IEEE 4-Byte-Real Wert (**VT \_ R4**).<br/> Weitere Informationen zum Arbeiten mit Arrays finden Sie unter [Abrufen von Vektor Typen](retrieving-vector-types.md).<br/> |
| <span id="SENSOR_DATA_TYPE_LIGHT_LEVEL_LUX"></span><span id="sensor_data_type_light_level_lux"></span><dl> <dt>**Sensor \_ Data \_ Type \_ Light \_ Level \_ Lux**</dt> <dt> (PID = 2)</dt> </dl>                            | **VT \_ R4**<br/> Beleuchtungs Ebene in Lux.<br/>                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_LIGHT_TEMPERATURE_KELVIN"></span><span id="sensor_data_type_light_temperature_kelvin"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Licht \_ Temperatur \_ Kelvin**</dt> <dt> (PID = 3)</dt> </dl> | **VT \_ R4**<br/> Farbtemperatur in Grad Kelvin.<br/>                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensoren. h</dt> </dl> |



 

 




