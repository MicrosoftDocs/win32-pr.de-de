---
description: Diese Konstanten werden in zwei Kontexten verwendet.
ms.assetid: 5c05a567-cc65-411e-b049-919a442c5c57
title: LINEPROXYREQUEST_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eba34a3a7f7b1f41f0c32783c4132afcfafef1aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354717"
---
# <a name="lineproxyrequest_-constants"></a>Lineproxyrequest- \_ Konstanten

Diese Konstanten werden in zwei Kontexten verwendet. Zuerst können Sie in einem Array von **DWORD** -Werten in der [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) -Struktur verwendet werden, die mit [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) übergeben wird, wenn die Option "lineopenoption" \_ angegeben wird, um anzugeben, welche Funktionen die Anwendung verarbeiten soll. Zweitens werden Sie in der [**Zeile \_ proxyrequest**](line-proxyrequest.md) verwendet, die von einer **line \_ proxyrequest** -Nachricht an die Handleranwendung übermittelt wird, um den Typ der zu verarbeitenden Anforderung und das Format der Daten im Puffer anzugeben.

<dl> <dt>

<span id="LINEPROXYREQUEST_AGENTSPECIFIC"></span><span id="lineproxyrequest_agentspecific"></span>**lineproxyrequest- \_ agentspezifisch**
</dt> <dd> <dl> <dt>



Ist [**lineagentspecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)zugeordnet.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_CREATEAGENT"></span><span id="lineproxyrequest_createagent"></span>**lineproxyrequest- \_ kreateagent**
</dt> <dd> <dl> <dt>



Verknüpft mit [**linecreateagent**](/windows/desktop/api/Tapi/nf-tapi-linecreateagenta).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_CREATEAGENTSESSION"></span><span id="lineproxyrequest_createagentsession"></span>**lineproxyrequest- \_ Sitzung**
</dt> <dd> <dl> <dt>



Verknüpft mit [**linecreateagentsession**](/windows/desktop/api/Tapi/nf-tapi-linecreateagentsessiona).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTACTIVITYLIST"></span><span id="lineproxyrequest_getagentactivitylist"></span>**lineproxyrequest \_ getagentactivitylist**
</dt> <dd> <dl> <dt>



Ist [**linegetagentactivitylist**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista)zugeordnet.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTCAPS"></span><span id="lineproxyrequest_getagentcaps"></span>**lineproxyrequest \_ getagentcaps**
</dt> <dd> <dl> <dt>



Mit [**linegetagentcaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)verknüpft.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTGROUPLIST"></span><span id="lineproxyrequest_getagentgrouplist"></span>**lineproxyrequest \_ getagentgrouplist**
</dt> <dd> <dl> <dt>



Ist [**linegetagentgrouplist**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)zugeordnet.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTINFO"></span><span id="lineproxyrequest_getagentinfo"></span>**lineproxyrequest \_ getagentinfo**
</dt> <dd> <dl> <dt>



Ist [**linegetagentinfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo)zugeordnet.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTSESSIONINFO"></span><span id="lineproxyrequest_getagentsessioninfo"></span>**lineproxyrequest \_ getagentsessioninfo**
</dt> <dd> <dl> <dt>



Ist [**linegetagentsessioninfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo)zugeordnet.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTSESSIONLIST"></span><span id="lineproxyrequest_getagentsessionlist"></span>**lineproxyrequest \_ getagentsessionlist**
</dt> <dd> <dl> <dt>



Ist [**linegetagentsessionlist**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessionlist)zugeordnet.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTSTATUS"></span><span id="lineproxyrequest_getagentstatus"></span>**lineproxyrequest \_ getagentstatus**
</dt> <dd> <dl> <dt>



Ist [**linegetagentstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)zugeordnet.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETGROUPLIST"></span><span id="lineproxyrequest_getgrouplist"></span>**"lineproxyrequest" \_ getgrouplist**
</dt> <dd> <dl> <dt>



Ist [**linegetgrouplist**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista)zugeordnet.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETQUEUEINFO"></span><span id="lineproxyrequest_getqueueinfo"></span>**lineproxyrequest \_ getqueueinfo**
</dt> <dd> <dl> <dt>



Ist [**linegetqueueinfo**](/windows/desktop/api/Tapi/nf-tapi-linegetqueueinfo)zugeordnet.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETQUEUELIST"></span><span id="lineproxyrequest_getqueuelist"></span>**lineproxyrequest \_ getqueuelist**
</dt> <dd> <dl> <dt>



[**Ist linegetqueuelist**](/windows/desktop/api/Tapi/nf-tapi-linegetqueuelista)zugeordnet.


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTACTIVITY"></span><span id="lineproxyrequest_setagentactivity"></span>**lineproxyrequest \_ setagentactivity**
</dt> <dd> <dl> <dt>



Verknüpft mit [**linesetagentactivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTGROUP"></span><span id="lineproxyrequest_setagentgroup"></span>**lineproxyrequest \_ setagentgroup**
</dt> <dd> <dl> <dt>



Verknüpft mit [**linesetagentgroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setagentmeasurementperiod"></span>**lineproxyrequest \_ setagentmessrementperiod**
</dt> <dd> <dl> <dt>



Zugeordnet mit [**linesetagentmessrementperiod**](/windows/desktop/api/Tapi/nf-tapi-linesetagentmeasurementperiod).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTSESSIONSTATE"></span><span id="lineproxyrequest_setagentsessionstate"></span>**lineproxyrequest \_ setagentsessionstate**
</dt> <dd> <dl> <dt>



Verknüpft mit [**linesetagentsessionstate**](/windows/desktop/api/Tapi/nf-tapi-linesetagentsessionstate).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTSTATE"></span><span id="lineproxyrequest_setagentstate"></span>**lineproxyrequest \_ setagentstate**
</dt> <dd> <dl> <dt>



Verknüpft mit [**linesetagentstate**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTSTATEEX"></span><span id="lineproxyrequest_setagentstateex"></span>**lineproxyrequest \_ setagentstateex**
</dt> <dd> <dl> <dt>



Verknüpft mit [**linesetagentstateex**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstateex).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETQUEUEMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setqueuemeasurementperiod"></span>**lineproxyrequest \_ setqueuemessrementperiod**
</dt> <dd> <dl> <dt>



Zugeordnet mit [**linesetqueuemessrementperiod**](/windows/desktop/api/Tapi/nf-tapi-linesetqueuemeasurementperiod).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Callcenterkonstanten](call-center-constants.md)
</dt> <dt>

[Callcenter-Funktionen](call-center-functions.md)
</dt> </dl>

 

 




