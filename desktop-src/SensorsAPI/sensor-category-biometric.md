---
description: Die \_ Kategorie SENSOR CATEGORY \_ BIOMETRIC enthält Sensoren, die Informationen über Lebendwesen bereitstellen.
ms.assetid: dfc7ad46-c13b-46d1-8854-0d93ecaac55a
title: SENSOR_CATEGORY_BIOMETRIC (Sensors.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1551a82e359d2277c8b46f227d7a72660b1419b3ba3ddfcf58bdd4ac1de5425b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889576"
---
# <a name="sensor_category_biometric"></a>SENSORKATEGORIE \_ \_ BIOMETRIE

Die \_ Kategorie SENSOR CATEGORY \_ BIOMETRIC enthält Sensoren, die Informationen über Lebendwesen bereitstellen.

**Plattformdefinierte Sensortypen**

Diese Kategorie umfasst die folgenden plattformdefinierte Sensortypen.



| Sensortyp                                                                                                                                                                                                                                                                                           | BESCHREIBUNG                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------|
| <span id="SENSOR_TYPE_HUMAN_PRESENCE"></span><span id="sensor_type_human_presence"></span><dl> <dt>**SENSOR \_ TYPE \_ HUMAN \_ PRESENCE**</dt> <dt>{C138C12B-AD52-451C-9375-87F518FF10C6}</dt> </dl>    | Sensoren, die menschliche Präsenz erkennen.<br/>  |
| <span id="SENSOR_TYPE_HUMAN_PROXIMITY"></span><span id="sensor_type_human_proximity"></span><dl> <dt>**SENSOR \_ TYPE \_ HUMAN \_ PROXIMITY**</dt> <dt>{5220DAE9-3179-4430-9F90-06266D2A34DE}</dt> </dl> | Sensoren, die menschliche Nähe erkennen.<br/> |
| <span id="SENSOR_TYPE_TOUCH"></span><span id="sensor_type_touch"></span><dl> <dt>**SENSOR \_ TYPE \_ TOUCH**</dt> <dt>{17DB3018-06C4-4F7D-81AF-9274B7599C27}</dt> </dl>                                | Touchsensoren.<br/>                       |



**Plattformdefinierte Datenfelder**

Plattformdefinierte Eigenschaftsschlüssel für diese Kategorie basieren auf DER \_ BIOMETRISCHEN BENUTZEROBERFLÄCHE DES \_ SENSORDATENTYPs: \_ \_

{2299288A-6D9E-4B0B-B7EC-3528F89E40AF}

Diese Kategorie umfasst die folgenden plattformdefinierte Datenfelder.



| Datenfeldname und PID                                                                                                                                                                                                                                                                                         | BESCHREIBUNG                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_HUMAN_PRESENCE"></span><span id="sensor_data_type_human_presence"></span><dl> <dt>**SENSOR \_ \_DATENTYP \_ MENSCHLICHE \_ PRÄSENZ**</dt> <dt>(PID = 2)</dt> </dl>                          | **VT \_ BOOL**<br/> **TRUE,** wenn ein Mensch den Computer verwendet.<br/>                           |
| <span id="SENSOR_DATA_TYPE_HUMAN_PROXIMITY_METERS"></span><span id="sensor_data_type_human_proximity_meters"></span><dl> <dt>**SENSOR \_ \_DATENTYP: \_ \_ NÄHERUNGSZÄHLER \_**</dt> FÜR MENSCHEN <dt>(PID = 3)</dt> </dl> | **VT \_ R4**<br/> Abstand zwischen einem Menschen und dem Computer in Metern.<br/>                    |
| <span id="SENSOR_DATA_TYPE_TOUCH_STATE"></span><span id="sensor_data_type_touch_state"></span><dl> <dt>**SENSOR \_ TOUCHZUSTAND DES \_ \_ \_ DATENTYPS**</dt> <dt>(PID = 4)</dt> </dl>                                   | **VT \_ BOOL**<br/> **TRUE,** wenn der Touchsensor berührt wird; Andernfalls **FALSE**.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensors.h</dt> </dl> |



 

 




