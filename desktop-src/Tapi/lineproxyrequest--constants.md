---
description: Diese Konstanten werden in zwei Kontexten verwendet.
ms.assetid: 5c05a567-cc65-411e-b049-919a442c5c57
title: LINEPROXYREQUEST_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b869027bd801079774f2caf35de47bcf6d883dd568b30f66bd4bda37fae43c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003038"
---
# <a name="lineproxyrequest_-constants"></a>\_LINEPROXYREQUEST-Konstanten

Diese Konstanten werden in zwei Kontexten verwendet. Erstens können sie in einem Array von **DWORD-Werten** in der [**LINECALLPARAMS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) verwendet werden, die mit [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) übergeben werden, wenn die OPTION LINEOPENOPTION \_ PROXY angegeben wird, um anzugeben, welche Funktionen die Anwendung behandeln möchte. Zweitens werden sie in der [**LINE \_ PROXYREQUEST**](line-proxyrequest.md) verwendet, die von einer **LINE \_ PROXYREQUEST-Nachricht** an die Handleranwendung übergeben wird, um den Typ der zu verarbeitenden Anforderung und das Format der Daten im Puffer anzugeben.

<dl> <dt>

<span id="LINEPROXYREQUEST_AGENTSPECIFIC"></span><span id="lineproxyrequest_agentspecific"></span>**LINEPROXYREQUEST \_ AGENTSPECIFIC**
</dt> <dd> <dl> <dt>



Zugeordnet zu [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_CREATEAGENT"></span><span id="lineproxyrequest_createagent"></span>**LINEPROXYREQUEST \_ CREATEAGENT**
</dt> <dd> <dl> <dt>



Ist [**lineCreateAgent**](/windows/desktop/api/Tapi/nf-tapi-linecreateagenta)zugeordnet.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_CREATEAGENTSESSION"></span><span id="lineproxyrequest_createagentsession"></span>**LINEPROXYREQUEST \_ CREATEAGENTSESSION**
</dt> <dd> <dl> <dt>



Zugeordnet zu [**lineCreateAgentSession**](/windows/desktop/api/Tapi/nf-tapi-linecreateagentsessiona).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTACTIVITYLIST"></span><span id="lineproxyrequest_getagentactivitylist"></span>**LINEPROXYREQUEST \_ GETAGENTACTIVITYLIST**
</dt> <dd> <dl> <dt>



Zugeordnet zu [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTCAPS"></span><span id="lineproxyrequest_getagentcaps"></span>**LINEPROXYREQUEST \_ GETAGENTCAPS**
</dt> <dd> <dl> <dt>



Zugeordnet zu [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTGROUPLIST"></span><span id="lineproxyrequest_getagentgrouplist"></span>**LINEPROXYREQUEST \_ GETAGENTGROUPLIST**
</dt> <dd> <dl> <dt>



Wird [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)zugeordnet.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTINFO"></span><span id="lineproxyrequest_getagentinfo"></span>**LINEPROXYREQUEST \_ GETAGENTINFO**
</dt> <dd> <dl> <dt>



Wird [**lineGetAgentInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo)zugeordnet.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTSESSIONINFO"></span><span id="lineproxyrequest_getagentsessioninfo"></span>**LINEPROXYREQUEST \_ GETAGENTSESSIONINFO**
</dt> <dd> <dl> <dt>



Zugeordnet zu [**lineGetAgentSessionInfo.**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo)


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTSESSIONLIST"></span><span id="lineproxyrequest_getagentsessionlist"></span>**LINEPROXYREQUEST \_ GETAGENTSESSIONLIST**
</dt> <dd> <dl> <dt>



Wird [**lineGetAgentSessionList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessionlist)zugeordnet.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTSTATUS"></span><span id="lineproxyrequest_getagentstatus"></span>**LINEPROXYREQUEST \_ GETAGENTSTATUS**
</dt> <dd> <dl> <dt>



Wird [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)zugeordnet.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETGROUPLIST"></span><span id="lineproxyrequest_getgrouplist"></span>**LINEPROXYREQUEST \_ GETGROUPLIST**
</dt> <dd> <dl> <dt>



Zugeordnet zu [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETQUEUEINFO"></span><span id="lineproxyrequest_getqueueinfo"></span>**LINEPROXYREQUEST \_ GETQUEUEINFO**
</dt> <dd> <dl> <dt>



Ist [**lineGetQueueInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetqueueinfo)zugeordnet.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETQUEUELIST"></span><span id="lineproxyrequest_getqueuelist"></span>**LINEPROXYREQUEST \_ GETQUEPROXYIST**
</dt> <dd> <dl> <dt>



Zugeordnet zu [**lineGetQueueList**](/windows/desktop/api/Tapi/nf-tapi-linegetqueuelista).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTACTIVITY"></span><span id="lineproxyrequest_setagentactivity"></span>**LINEPROXYREQUEST \_ SETAGENTACTIVITY**
</dt> <dd> <dl> <dt>



Zugeordnet zu [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTGROUP"></span><span id="lineproxyrequest_setagentgroup"></span>**LINEPROXYREQUEST \_ SETAGENTGROUP**
</dt> <dd> <dl> <dt>



Wird [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup)zugeordnet.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setagentmeasurementperiod"></span>**LINEPROXYREQUEST \_ SETAGENTMEASUREMENTPERIOD**
</dt> <dd> <dl> <dt>



Wird [**lineSetAgentMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetagentmeasurementperiod)zugeordnet.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTSESSIONSTATE"></span><span id="lineproxyrequest_setagentsessionstate"></span>**LINEPROXYREQUEST \_ SETAGENTSESSIONSTATE**
</dt> <dd> <dl> <dt>



Zugeordnet zu [**lineSetAgentSessionState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentsessionstate).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTSTATE"></span><span id="lineproxyrequest_setagentstate"></span>**LINEPROXYREQUEST \_ SETAGENTSTATE**
</dt> <dd> <dl> <dt>



Wird [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)zugeordnet.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTSTATEEX"></span><span id="lineproxyrequest_setagentstateex"></span>**LINEPROXYREQUEST \_ SETAGENTSTATEEX**
</dt> <dd> <dl> <dt>



Ist [**lineSetAgentStateEx**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstateex)zugeordnet.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETQUEUEMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setqueuemeasurementperiod"></span>**LINEPROXYREQUEST \_ SETQUEUEMEASUREMENTPERIOD**
</dt> <dd> <dl> <dt>



Zugeordnet zu [**lineSetQueueMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetqueuemeasurementperiod).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Callcenterkonstanten](call-center-constants.md)
</dt> <dt>

[Callcenterfunktionen](call-center-functions.md)
</dt> </dl>

 

 




