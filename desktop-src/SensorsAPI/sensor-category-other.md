---
description: Die Kategorie \_ \_ andere Kategorie des Sensors enthält Sensoren, die die benutzerdefinierte Klasse im HID-Klassen Treiber unterstützen.
ms.assetid: 866F7BF4-15CC-4F69-9510-B5858D47C4D0
title: SENSOR_CATEGORY_OTHER (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e26ece66ae74e873c48cd973cc447beec2dd8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041666"
---
# <a name="sensor_category_other"></a>\_andere Sensor Kategorie \_

Die Kategorie \_ \_ andere Kategorie des Sensors enthält Sensoren, die die benutzerdefinierte Klasse im HID-Klassen Treiber unterstützen.

<dl> <dt>

<span id="SENSOR_TYPE_CUSTOM"></span><span id="sensor_type_custom"></span>**\_ \_ benutzerdefinierter Sensortyp**
</dt> <dd> <dl> <dt>

{E83AF229-8640-4D18-A213-E22675EBB2C3}
</dt> <dt>



Benutzerdefinierter Sensor, der die benutzerdefinierte-Klasse im HID-Klassen Treiber unterstützt.


</dt> </dl> </dd> </dl>

**Platt Form definierte Datenfelder**

Platt Form definierte Eigenschafts Schlüssel für diese Kategorie basieren auf der \_ \_ \_ benutzerdefinierten GUID des Sensor Datentyps \_ :

{B14C764F-07CF-41E8-9D82-EBE3D0776A6F}

Diese Kategorie enthält die folgenden Platt Form definierten Datenfelder.



| Name und PID des Daten Felds                                                                                                                                                                                                                                                                                    | BESCHREIBUNG                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CUSTOM_USAGE"></span><span id="sensor_data_type_custom_usage"></span><dl> <dt>**Sensor \_ \_ \_ Benutzerdefinierte \_ Verwendung des Datentyps**</dt> <dt> (PID = 5)</dt> </dl>                          | **VT \_ UI4**<br/> Eine versteckte Verwendung, die zur Unterscheidung mehrerer, benutzerdefinierter Sensoren verwendet werden kann.<br/> |
| <span id="SENSOR_DATA_TYPE_CUSTOM_BOOLEAN_ARRAY"></span><span id="sensor_data_type_custom_boolean_array"></span><dl> <dt>**Sensor \_ \_ \_ Benutzerdefiniertes \_ Boolesches \_ Array des Datentyps**</dt> <dt> (PID = 6)</dt> </dl> | **VT \_ UI4**<br/> Ein Array von booleschen Werten für einen angegebenen benutzerdefinierten Sensor.<br/>                  |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE1"></span><span id="sensor_data_type_custom_value1"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Benutzer definiert \_ value1**</dt> <dt> (PID = 7)</dt> </dl>                       | **VT \_ UI4 \| \| VT \_ R4**<br/> Einer von sechs verfügbaren Werten für einen angegebenen benutzerdefinierten Sensor.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE2"></span><span id="sensor_data_type_custom_value2"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Benutzer definiert \_ value2**</dt> <dt> (PID = 8)</dt> </dl>                       | **VT \_ UI4 \| \| VT \_ R4**<br/> Einer von sechs verfügbaren Werten für einen angegebenen benutzerdefinierten Sensor.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE3"></span><span id="sensor_data_type_custom_value3"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Benutzer definiert \_ Wert3**</dt> <dt> (PID = 9)</dt> </dl>                       | **VT \_ UI4 \| \| VT \_ R4**<br/> Einer von sechs verfügbaren Werten für einen angegebenen benutzerdefinierten Sensor.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE4"></span><span id="sensor_data_type_custom_value4"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Benutzer definiert \_ VALUE4**</dt> <dt> (PID = 10)</dt> </dl>                      | **VT \_ UI4 \| \| VT \_ R4**<br/> Einer von sechs verfügbaren Werten für einen angegebenen benutzerdefinierten Sensor.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE5"></span><span id="sensor_data_type_custom_value5"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Benutzer definiert \_ VALUE5**</dt> <dt> (PID = 11)</dt> </dl>                      | **VT \_ UI4 \| \| VT \_ R4**<br/> Einer von sechs verfügbaren Werten für einen angegebenen benutzerdefinierten Sensor.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE6"></span><span id="sensor_data_type_custom_value6"></span><dl> <dt>**Sensor \_ \_Datentyp \_ Benutzer definiert \_ VALUE6**</dt> <dt> (PID = 12)</dt> </dl>                      | **VT \_ UI4 \| \| VT \_ R4**<br/> Einer von sechs verfügbaren Werten für einen angegebenen benutzerdefinierten Sensor.<br/>       |



## <a name="remarks"></a>Bemerkungen

Ein Sensor, der die generische Klasse im HID-Klassen Treiber unterstützt, wird einer der anderen definierten Kategorien (biometrische, elektrisch, Umwelt usw.) zugeordnet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensoren. h</dt> </dl> |



 

 




