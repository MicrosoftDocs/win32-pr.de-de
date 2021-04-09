---
description: Die Kategorie biometrische Kategorie des Sensors \_ \_ enthält Sensoren, die Informationen zu Lebewesen bereitstellen.
ms.assetid: dfc7ad46-c13b-46d1-8854-0d93ecaac55a
title: SENSOR_CATEGORY_BIOMETRIC (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71660c7bc94037c21502c91e017a8eba369766a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128745"
---
# <a name="sensor_category_biometric"></a>Sensor \_ Kategorie \_ biometrische

Die Kategorie biometrische Kategorie des Sensors \_ \_ enthält Sensoren, die Informationen zu Lebewesen bereitstellen.

**Platt Form definierte Sensor Typen**

Diese Kategorie enthält die folgenden Platt Form definierten Sensortypen.



| Sensortyp                                                                                                                                                                                                                                                                                           | BESCHREIBUNG                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------|
| <span id="SENSOR_TYPE_HUMAN_PRESENCE"></span><span id="sensor_type_human_presence"></span><dl> <dt>**Sensor \_ \_Typpräsenz \_ von Menschen**</dt> <dt>{C138C12B-AD52-451C-9375-87F518FF10C6}</dt> </dl>    | Sensoren, die die menschliche Präsenz erkennen.<br/>  |
| <span id="SENSOR_TYPE_HUMAN_PROXIMITY"></span><span id="sensor_type_human_proximity"></span><dl> <dt>**Sensor \_ Type \_ Human \_ near**</dt> <dt>{5220dae9-3179-4430-9F 90-06266d2a34de}</dt> </dl> | Sensoren, mit denen die menschliche Nähe erkannt wird.<br/> |
| <span id="SENSOR_TYPE_TOUCH"></span><span id="sensor_type_touch"></span><dl> <dt>**Sensor \_ Geben \_**</dt> Sie "berühren <dt>{17db3018-06c4-4b7599c27}</dt> " ein. </dl>                                | Touchscreen-Sensoren.<br/>                       |



**Platt Form definierte Datenfelder**

Platt Form definierte Eigenschafts Schlüssel für diese Kategorie basieren auf der \_ \_ \_ biometrischen GUID des Sensor-Datentyps \_ :

{2299288a-6d9e-4b0b-b7ec-3528f 89e40af}

Diese Kategorie enthält die folgenden Platt Form definierten Datenfelder.



| Name und PID des Daten Felds                                                                                                                                                                                                                                                                                         | BESCHREIBUNG                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_HUMAN_PRESENCE"></span><span id="sensor_data_type_human_presence"></span><dl> <dt>**Sensor \_ \_ \_ \_ Anwesenheit des Datentyps**</dt> <dt>(PID = 2)</dt> </dl>                          | **VT \_ bool**<br/> **True** , wenn ein Benutzer den Computer verwendet.<br/>                           |
| <span id="SENSOR_DATA_TYPE_HUMAN_PROXIMITY_METERS"></span><span id="sensor_data_type_human_proximity_meters"></span><dl> <dt>**Sensor \_ Datentyp: \_ \_ menschliche \_ near- \_ Zähler**</dt> <dt>(PID = 3)</dt> </dl> | **VT \_ R4**<br/> Abstand zwischen einem Menschen und dem Computer in Meter.<br/>                    |
| <span id="SENSOR_DATA_TYPE_TOUCH_STATE"></span><span id="sensor_data_type_touch_state"></span><dl> <dt>**Sensor \_ Datentyp- \_ \_ Berührungs \_ Zustand**</dt> <dt>(PID = 4)</dt> </dl>                                   | **VT \_ bool**<br/> **True** , wenn der TouchSensor berührt wird. andernfalls **false**.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensoren. h</dt> </dl> |



 

 




