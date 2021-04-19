---
description: Die Windows-Sensor-und-Location-Plattform definiert Konstanten für Treiber Ereignisse. Sensor manfuactureres können auch Ihre eigenen Konstanten definieren.
ms.assetid: ca61c912-bce5-4e41-ab48-40615d5b93ba
title: Ereignis Konstanten (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9fb3ced92c1fe263538f2ce27c3fc65fdd7676
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364090"
---
# <a name="event-constants-sensorsh"></a>Ereignis Konstanten (Sensors. h)

Die Windows-Sensor-und-Location-Plattform definiert Konstanten für Treiber Ereignisse. Sensor manfuactureres können auch Ihre eigenen Konstanten definieren.

**Sensor Ereignis Typen**

Die Plattform definiert die folgenden Typen von Sensor Ereignis Typen.



| Sensor Ereignistyp                                                                                                                                                                                                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_ACCELEROMETER_SHAKE"></span><span id="sensor_event_accelerometer_shake"></span><dl> <dt>**Sensor \_ Ereignis \_ Beschleunigungsmesser- \_ Shake**</dt> <dt>{825 f 94-0 ecb5c99d915}</dt> </dl> | Gibt an, dass das Gerät geschüttelt wurde.<br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_DATA_UPDATED"></span><span id="sensor_event_data_updated"></span><dl> <dt>**Sensor \_ Ereignis \_ Daten \_ aktualisiert**</dt> <dt>{2ed0f 2a4-0087-41d3-87dB-6773370b3c88}</dt> </dl>                      | Gibt an, dass neue Daten verfügbar sind.<br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_PROPERTY_CHANGED"></span><span id="sensor_event_property_changed"></span><dl> <dt>**Sensor \_ Ereignis \_ Eigenschaft \_ geändert**</dt> <dt>{2358f 099-84c9-4d3d-90df-c2421e2b2045}</dt> </dl>          | Gibt an, dass sich ein Eigenschafts Wert geändert hat. Überprüfen Sie die Schnittstelle [iportablewavicevalues](/previous-versions//ms740012(v=vs.85)) , die über den Parameter " *Peer Event Data* " an [**OnEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent)übergeben wird, um zu bestimmen, welche Eigenschaft geändert wurde, und den neuen Wert.<br/> |
| <span id="SENSOR_EVENT_STATE_CHANGED"></span><span id="sensor_event_state_changed"></span><dl> <dt>**Sensor \_ Ereignis \_ Status \_ geändert**</dt> <dt>{BFD96016-6BD7-4560-AD34-F2F6607E8F81}</dt> </dl>                   | Gibt eine Änderung des Betriebsstatus an, z. b. vom Sensor \_ Status \_ Initialisierung in den Sensor \_ Zustand \_ bereit.<br/>                                                                                                                                                                                            |



**PropertyKeys des Sensor Ereignisses**

Platt Form definierte Eigenschafts Schlüssel für Ereignisse basieren auf der folgenden GUID:

{64346e30-8728-4b34-bdf6-4l52442c5c28}

Die Sensorplattform definiert die folgenden **PropertyKeys**, die Sensor Ereignis Parameter identifizieren.



| PropertyKey und PID des Sensor Ereignisses                                                                                                                                                                                                                                                      | BESCHREIBUNG                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_PARAMETER_EVENT_ID"></span><span id="sensor_event_parameter_event_id"></span><dl> <dt>**Sensor \_ Ereignis \_ Parameter \_ Ereignis- \_ ID**</dt> <dt>(PID = 2)</dt> </dl> | Gibt an, dass der **GUID** -Wert in [iportabledevicevalues](/previous-versions//ms740012(v=vs.85)) eine Ereignistyp-ID ist, z \_ . b \_ . aktualisierte Sensor Ereignisdaten \_ .<br/> |
| <span id="SENSOR_EVENT_PARAMETER_STATE"></span><span id="sensor_event_parameter_state"></span><dl> <dt>**Sensor \_ \_ \_ Status des Ereignis Parameters**</dt> <dt>(PID = 3)</dt> </dl>           | Gibt an, dass der Wert einer Ganzzahl ohne Vorzeichen in **iportableendvicevalues** ein Sensor Zustand ist, z. b. der Sensor \_ Status \_ Ready.<br/>                                                  |



**PropertyKeys des Sensor Fehlers**

Platt Form definierte Eigenschafts Schlüssel für Fehler basieren auf der folgenden GUID:

{77112bcd-oce1-4f 43-b8b8-a88256adb4b3}

Die Sensorplattform reserviert diese GUID für die zukünftige Verwendung.

<dl></dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensoren. h</dt> </dl> |



 

