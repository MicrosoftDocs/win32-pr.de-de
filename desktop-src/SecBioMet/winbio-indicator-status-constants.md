---
title: WINBIO_INDICATOR_STATUS Konstanten (Winbio \_ types.h)
description: Legen Sie ein Indikatorlicht fest.
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
ms.openlocfilehash: 9fd05d279bd11eafda89eed436c94d6141e97ad0eb9d2fc426d5c89000f36414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910013"
---
# <a name="winbio_indicator_status-constants"></a>\_ \_ WINBIO-INDIKATORSTATUSkonst constants

Die folgenden Werte können verwendet werden, um ein Indikatorlicht zu setzen. Standardmäßig haben Sensoren kein Licht, aber Anwendungen können diese Werte verwenden, um Indikatorlichter zu aktivieren oder zu deaktivieren. Der **WINBIO \_ SENSOR \_ STATUS-Wert** enthält weitere Details zum Status einer Ein-/Aus-Indikatoranzeige. Weitere Informationen finden Sie in den folgenden Funktionen:

-   [**SensorAdapterSetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)
-   [**SensorAdapterGetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)
-   [**SensorAdapterQueryStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)



| Konstante                                                                                                                                                                            | BESCHREIBUNG                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------|
| <span id="WINBIO_INDICATOR_ON"></span><span id="winbio_indicator_on"></span><dl> <dt>**\_WINBIO-INDIKATOR \_ EIN**</dt> </dl>    | Das Sensoranzeigelicht ist ein.<br/>  |
| <span id="WINBIO_INDICATOR_OFF"></span><span id="winbio_indicator_off"></span><dl> <dt>**\_WINBIO-INDIKATOR \_ DEAKTIVIERT**</dt> </dl> | Das Sensoranzeigelicht ist ausgeschaltet.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (einschließlich Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungskonst constants](client-application-constants.md)
</dt> </dl>

 

 





