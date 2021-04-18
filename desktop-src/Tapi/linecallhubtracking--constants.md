---
description: Die linecallhubtracking- \_ Bitflag-Konstanten beschreiben den Typ der bereitgestellten callhub-Nachverfolgung.
ms.assetid: ad3c8d2e-f074-4db0-bb72-fb2181cbf687
title: LINECALLHUBTRACKING_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfae61e36551a7d186408c2c87e0727503540a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357670"
---
# <a name="linecallhubtracking_-constants"></a>Linecallhubtracking- \_ Konstanten

Die **linecallhubtracking \_** -Bitflag-Konstanten beschreiben den Typ der bereitgestellten callhub-Nachverfolgung.

<dl> <dt>

<span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**linecallhubtracking \_ allcalls**
</dt> <dd> <dl> <dt>



Die callhub-Nachverfolgung wird auf der Rufebene bereitgestellt.


</dt> </dl> </dd> <dt>

<span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**linecallhubtracking \_ None**
</dt> <dd> <dl> <dt>



Es wird keine callhub-Nachverfolgung bereitgestellt.


</dt> </dl> </dd> <dt>

<span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**linecallhubtracking- \_ providerlevel**
</dt> <dd> <dl> <dt>



Callhubs werden auf Dienstanbieter Ebene nachverfolgt. Aufrufe durch aufrufänderungen werden nicht gemeldet.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Wenn in dieser Datenstruktur Änderungen auftreten, wird eine [**Zeile \_ CallInfo**](line-callinfo.md) -Meldung an die Anwendung gesendet. Die Parameter für diese Nachricht sind ein Handle für den-Befehl und ein Hinweis auf das geänderte Informationselement. Die [**linecallhubtrackinginfo**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo) -Datenstruktur gibt an, welcher Nachverfolgungstyp bereitgestellt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,2<br/>                                                      |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_liniencallinfo**](line-callinfo.md)
</dt> <dt>

[**Linecallhubtrackinginfo**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo)
</dt> <dt>

[**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> </dl>

 

 




