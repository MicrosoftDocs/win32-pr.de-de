---
title: WINBIO_SENSOR_MODE Konstanten (winbio \_ types. h)
description: Legen Sie den Sensor Adapter Modus fest.
ms.assetid: fceaed5c-de59-4da7-9d7a-adeef353292f
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_UNKNOWN_MODE
- WINBIO_SENSOR_BASIC_MODE
- WINBIO_SENSOR_ADVANCED_MODE
- WINBIO_SENSOR_NAVIGATION_MODE
- WINBIO_SENSOR_SLEEP_MODE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fedf419a64b3629d0cccbcb3d56de31a4adf383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743672"
---
# <a name="winbio_sensor_mode-constants"></a>Winbio- \_ Sensor \_ Modus-Konstanten

Die folgenden Werte werden in der [**sensoradaptersetmode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) -Funktion verwendet, um den Sensor Adapter Modus festzulegen.



| Konstante                                                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_SENSOR_UNKNOWN_MODE"></span><span id="winbio_sensor_unknown_mode"></span><dl> <dt>**\_ \_ unbekannter \_ Modus des winbio-Sensors**</dt> </dl>          | Der Betriebsmodus ist nicht bekannt.<br/>                                                                                                                    |
| <span id="WINBIO_SENSOR_BASIC_MODE"></span><span id="winbio_sensor_basic_mode"></span><dl> <dt>**\_ \_ Basis \_ Modus des winbio-Sensors**</dt> </dl>                | Betreiben Sie den Sensor im Standardmodus. Der Sensor fungiert nur als Erfassungsgerät. Alle vorhandenen integrierten Verarbeitungs-oder Speicherfunktionen werden nicht verwendet.<br/> |
| <span id="WINBIO_SENSOR_ADVANCED_MODE"></span><span id="winbio_sensor_advanced_mode"></span><dl> <dt>**Erweiterter Modus des winbio- \_ Sensors \_ \_**</dt> </dl>       | Betreiben Sie den Sensor im erweiterten Modus. Der Sensor kann Beispiele erfassen und übereinstimmende und Speicherfunktionen ausführen.<br/>                                     |
| <span id="WINBIO_SENSOR_NAVIGATION_MODE"></span><span id="winbio_sensor_navigation_mode"></span><dl> <dt>**winbio- \_ Sensor- \_ Navigations \_ Modus**</dt> </dl> | Betreiben Sie den Sensor als Mauspad. Dies wird derzeit nicht unterstützt.<br/>                                                                                 |
| <span id="WINBIO_SENSOR_SLEEP_MODE"></span><span id="winbio_sensor_sleep_mode"></span><dl> <dt>**winbio- \_ Sensor-Standbymodus \_ \_**</dt> </dl>                | Betreiben Sie den Sensor im Energiesparmodus.<br/>                                                                                                                   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Anwendungs Konstanten](client-application-constants.md)
</dt> </dl>

 

 





