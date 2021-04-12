---
title: System Monitor. OnDblClick-Ereignis
description: Benachrichtigt Sie, wenn ein Benutzer mit der linken Maustaste auf die Diagramm Linie, die Histogrammleiste oder das Berichts Element doppelklickt.
ms.assetid: 06ad86ff-fcc0-4be5-a54c-7a6aa1147cf9
keywords:
- OnDblClick-Ereignis (Sysmon)
- OnDblClick-Ereignis (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse "sysmon", OnDblClick-Ereignis
topic_type:
- apiref
api_name:
- SystemMonitor.OnDblClick
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f21c6d67468ecb07bbe0fe83bec7b48a086571
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103838"
---
# <a name="systemmonitorondblclick-event"></a>System Monitor. OnDblClick-Ereignis

Benachrichtigt Sie, wenn ein Benutzer mit der linken Maustaste auf die Diagramm Linie, die Histogrammleiste oder das Berichts Element doppelklickt.

## <a name="syntax"></a>Syntax


```VB
SystemMonitor.OnDblClick( _
  ByRef index As Long _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in, out\]
</dt> <dd>

Index des ausgewählten Indikators im [**indikatorensammlungs Objekt**](counters.md) . Wenn kein Indikator ausgewählt wurde, wird der Indexwert 0 zurückgegeben. Andernfalls wird der Index des ausgewählten Zählers zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn dieses Ereignis ausgelöst wird, wird der vom Benutzer im Liniendiagramm und im Histogramm ausgewählte Wert auch im Legenden Bereich ausgewählt. Dies erleichtert es dem Benutzer des System Monitors, festzustellen, welcher Indikatoren ausgewählt wird, wenn mehrere Werte angezeigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





