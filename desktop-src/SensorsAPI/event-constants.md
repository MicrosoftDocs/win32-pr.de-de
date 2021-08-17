---
description: Die Windows Sensor- und Standortplattform definiert Konstanten für Treiberereignisse. Sensor-Manfuactureres können auch ihre eigenen Konstanten definieren.
ms.assetid: ca61c912-bce5-4e41-ab48-40615d5b93ba
title: Ereigniskonst constants (Sensors.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1b16be770777c8e679e74123ce1c40c385893afee11ff3792dd58df007ae4c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890228"
---
# <a name="event-constants-sensorsh"></a>Ereigniskonst constants (Sensors.h)

Die Windows Sensor- und Standortplattform definiert Konstanten für Treiberereignisse. Sensor-Manfuactureres können auch ihre eigenen Konstanten definieren.

**Sensorereignistypen**

Die Plattform definiert die folgenden Sensorereignistypbezeichner.



| Sensorereignistyp                                                                                                                                                                                                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_ACCELEROMETER_SHAKE"></span><span id="sensor_event_accelerometer_shake"></span><dl> <dt>**SENSOR \_ EVENT \_ ACCELEROMETER \_ SHAKE**</dt> <dt>{825F5A94-0F48-4396-9CA0-6ECB5C99D915}</dt> </dl> | Gibt an, dass das Gerät gehakt wurde.<br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_DATA_UPDATED"></span><span id="sensor_event_data_updated"></span><dl> <dt>**SENSOR \_ EREIGNISDATEN \_ \_ AKTUALISIERT**</dt> <dt>{2ED0F2A4-0087-41D3-87DB-6773370B3C88}</dt> </dl>                      | Gibt an, dass neue Daten verfügbar sind.<br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_PROPERTY_CHANGED"></span><span id="sensor_event_property_changed"></span><dl> <dt>**SENSOR \_ EVENT \_ PROPERTY \_ CHANGED**</dt> <dt>{2358F099-84C9-4D3D-90DF-C2421E2B2045}</dt> </dl>          | Gibt an, dass sich ein Eigenschaftswert geändert hat. Überprüfen Sie [die IPortableDeviceValues-Schnittstelle,](/previous-versions//ms740012(v=vs.85)) die über den *pEventData-Parameter* an [**OnEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent)übergeben wird, um zu bestimmen, welche Eigenschaft und deren neuer Wert geändert wurden.<br/> |
| <span id="SENSOR_EVENT_STATE_CHANGED"></span><span id="sensor_event_state_changed"></span><dl> <dt>**SENSOR \_ EREIGNISZUSTAND \_ \_ GEÄNDERT**</dt> <dt>{BFD96016-6BD7-4560-AD34-F2F6607E8F81}</dt> </dl>                   | Gibt eine Änderung des Betriebszustands an, z. B. von SENSOR \_ STATE \_ INITIALIZING in SENSOR \_ STATE \_ READY.<br/>                                                                                                                                                                                            |



**SensorereignisEIGENSCHAFTKEYs**

Plattformdefinierte Eigenschaftsschlüssel für Ereignisse basieren auf der folgenden GUID:

{64346E30-8728-4B34-BDF6-4F52442C5C28}

Die Sensorplattform definiert die folgenden **PROPERTYKEY-Werte,** die Sensorereignisparameter identifizieren.



| Sensorereignis PROPERTYKEY und PID                                                                                                                                                                                                                                                      | BESCHREIBUNG                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_PARAMETER_EVENT_ID"></span><span id="sensor_event_parameter_event_id"></span><dl> <dt>**SENSOR \_ \_ \_ \_ EREIGNISPARAMETER-EREIGNIS-ID**</dt> <dt>(PID = 2)</dt> </dl> | Gibt an, **dass der GUID-Wert** in [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) eine Ereignistyp-ID ist, z. B. SENSOR \_ EVENT DATA \_ \_ UPDATED.<br/> |
| <span id="SENSOR_EVENT_PARAMETER_STATE"></span><span id="sensor_event_parameter_state"></span><dl> <dt>**SENSOR \_ EVENT \_ PARAMETER \_ STATE**</dt> <dt>(PID = 3)</dt> </dl>           | Gibt an, dass der ganzzahlige Wert ohne Vorzeichen in **IPortableDeviceValues** ein Sensorzustand ist, z. B. SENSOR \_ STATE \_ READY.<br/>                                                  |



**Sensorfehler PROPERTYKEYs**

Plattformdefinierte Eigenschaftsschlüssel für Fehler basieren auf der folgenden GUID:

{77112BCD-FCE1-4f43-B8B8-A88256ADB4B3}

Die Sensorplattform reserviert diese GUID für die zukünftige Verwendung.

<dl></dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensors.h</dt> </dl> |



 

