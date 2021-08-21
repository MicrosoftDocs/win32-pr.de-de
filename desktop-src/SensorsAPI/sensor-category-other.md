---
description: Die Kategorie SENSOR \_ CATEGORY \_ OTHER enthält Sensoren, die die Custom-Klasse im HID-Klassentreiber unterstützen.
ms.assetid: 866F7BF4-15CC-4F69-9510-B5858D47C4D0
title: SENSOR_CATEGORY_OTHER (Sensors.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a16fb192924defc3437d3ca60c85d80864831f8738ac75f67c1cf65e4f60b3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117968737"
---
# <a name="sensor_category_other"></a>SENSORKATEGORIE \_ \_ SONSTIGE

Die Kategorie SENSOR \_ CATEGORY \_ OTHER enthält Sensoren, die die Custom-Klasse im HID-Klassentreiber unterstützen.

<dl> <dt>

<span id="SENSOR_TYPE_CUSTOM"></span><span id="sensor_type_custom"></span>**SENSORTYP \_ \_ BENUTZERDEFINIERT**
</dt> <dd> <dl> <dt>

{E83AF229-8640-4D18-A213-E22675EBB2C3}
</dt> <dt>



Benutzerdefinierter Sensor, der die Custom-Klasse im HID-Klassentreiber unterstützt.


</dt> </dl> </dd> </dl>

**Plattformdefinierte Datenfelder**

Plattformdefinierte Eigenschaftsschlüssel für diese Kategorie basieren auf der \_ \_ \_ BENUTZERDEFINIERTEN GUID SENSOR DATA \_ TYPE:

{B14C764F-07CF-41E8-9D82-EBE3D0776A6F}

Diese Kategorie umfasst die folgenden plattformdefinierte Datenfelder.



| Datenfeldname und PID                                                                                                                                                                                                                                                                                    | Beschreibung                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CUSTOM_USAGE"></span><span id="sensor_data_type_custom_usage"></span><dl> <dt>**SENSOR \_ \_ \_ BENUTZERDEFINIERTE \_ NUTZUNG DES DATENTYPS**</dt> <dt> (PID = 5)</dt> </dl>                          | **VT \_ UI4**<br/> Eine HID-Verwendung, die verwendet werden kann, um mehrere benutzerdefinierte Sensoren zu unterscheiden.<br/> |
| <span id="SENSOR_DATA_TYPE_CUSTOM_BOOLEAN_ARRAY"></span><span id="sensor_data_type_custom_boolean_array"></span><dl> <dt>**SENSOR \_ \_ \_ BENUTZERDEFINIERTES \_ BOOLESCHES \_ ARRAY**</dt> DES DATENTYPS <dt> (PID = 6)</dt> </dl> | **VT \_ UI4**<br/> Ein Array boolescher Werte für einen bestimmten benutzerdefinierten Sensor.<br/>                  |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE1"></span><span id="sensor_data_type_custom_value1"></span><dl> <dt>**SENSOR \_ \_ \_ BENUTZERDEFINIERTER DATENTYP \_ VALUE1**</dt> <dt> (PID = 7)</dt> </dl>                       | **VT \_ UI4 \| \| VT \_ R4**<br/> Einer von sechs verfügbaren Werten für einen bestimmten benutzerdefinierten Sensor.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE2"></span><span id="sensor_data_type_custom_value2"></span><dl> <dt>**SENSOR \_ \_ \_ BENUTZERDEFINIERTER DATENTYP \_ VALUE2**</dt> <dt> (PID = 8)</dt> </dl>                       | **VT \_ UI4 \| \| VT \_ R4**<br/> Einer von sechs verfügbaren Werten für einen bestimmten benutzerdefinierten Sensor.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE3"></span><span id="sensor_data_type_custom_value3"></span><dl> <dt>**SENSOR \_ \_ \_ BENUTZERDEFINIERTER DATENTYP \_ VALUE3**</dt> <dt> (PID = 9)</dt> </dl>                       | **VT \_ UI4 \| \| VT \_ R4**<br/> Einer von sechs verfügbaren Werten für einen bestimmten benutzerdefinierten Sensor.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE4"></span><span id="sensor_data_type_custom_value4"></span><dl> <dt>**SENSOR \_ \_ \_ BENUTZERDEFINIERTER DATENTYP \_ VALUE4**</dt> <dt> (PID = 10)</dt> </dl>                      | **VT \_ UI4 \| \| VT \_ R4**<br/> Einer von sechs verfügbaren Werten für einen bestimmten benutzerdefinierten Sensor.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE5"></span><span id="sensor_data_type_custom_value5"></span><dl> <dt>**SENSOR \_ \_ \_ BENUTZERDEFINIERTER DATENTYP \_ VALUE5**</dt> <dt> (PID = 11)</dt> </dl>                      | **VT \_ UI4 \| \| VT \_ R4**<br/> Einer von sechs verfügbaren Werten für einen bestimmten benutzerdefinierten Sensor.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE6"></span><span id="sensor_data_type_custom_value6"></span><dl> <dt>**SENSOR \_ \_ \_ BENUTZERDEFINIERTER DATENTYP \_ VALUE6**</dt> <dt> (PID = 12)</dt> </dl>                      | **VT \_ UI4 \| \| VT \_ R4**<br/> Einer von sechs verfügbaren Werten für einen bestimmten benutzerdefinierten Sensor.<br/>       |



## <a name="remarks"></a>Hinweise

Ein Sensor, der die generische Klasse im HID-Klassentreiber unterstützt, wird einer der anderen definierten Kategorien (biometrische, elektrische, umgebungsbezogene usw.) zugeordnet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensors.h</dt> </dl> |



 

 




