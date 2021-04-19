---
title: WINBIO_INDICATOR_STATUS Konstanten (winbio \_ types. h)
description: Legen Sie eine Indikator Ampel fest.
ms.assetid: 1e00ff9d-6693-4763-8ac3-b42d2a3e987d
topic_type:
- apiref
api_name:
- WINBIO_INDICATOR_ON
- WINBIO_INDICATOR_OFF
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7693fbd2b9b37067738774d172f4bb482edb06e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343484"
---
# <a name="winbio_indicator_status-constants"></a>Winbio- \_ Indikator \_ Status Konstanten

Die folgenden Werte können verwendet werden, um eine Indikator Ampel festzulegen. Standardmäßig haben Sensoren keine Beleuchtung, aber Anwendungen können diese Werte verwenden, um Indikator Leuchten zu aktivieren oder zu deaktivieren. Der **\_ \_ Statuswert des winbio-Sensors** bietet weitere Details zum Status eines Indikator Lichts, das sich in befindet. Weitere Informationen finden Sie in den folgenden Funktionen:

-   [**Sensoradaptersetindikatorstatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)
-   [**Sensoradaptergetindikatorstatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)
-   [**Sensoradapterquerystatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)



| Konstante                                                                                                                                                                            | BESCHREIBUNG                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------|
| <span id="WINBIO_INDICATOR_ON"></span><span id="winbio_indicator_on"></span><dl> <dt>**winbio- \_ Indikator \_ für**</dt> </dl>    | Der Sensor Indikator Licht ist on.<br/>  |
| <span id="WINBIO_INDICATOR_OFF"></span><span id="winbio_indicator_off"></span><dl> <dt>**winbio- \_ Indikator \_ aus**</dt> </dl> | Die Sensor Indikator Beleuchtung ist deaktiviert.<br/> |



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

 

 





