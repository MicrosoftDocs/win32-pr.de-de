---
title: SystemMonitor.OnDblClick-Ereignis
description: Benachrichtigt Sie, wenn ein Benutzer mit der linken Maustaste auf die Diagrammlinie, die Histogrammleiste oder das Berichtselement doppelklickt.
ms.assetid: 06ad86ff-fcc0-4be5-a54c-7a6aa1147cf9
keywords:
- SysMon-Ereignis "OnDblClick"
- OnDblClick-Ereignis SysMon , SystemMonitor-Klasse
- SystemMonitor-Klasse SysMon , OnDblClick-Ereignis
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
ms.openlocfilehash: 37ef829fad368e7d8cf3b65ab70db4600f6d635b1d36bcc5e3f50fcdbaf429a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883959"
---
# <a name="systemmonitorondblclick-event"></a>SystemMonitor.OnDblClick-Ereignis

Benachrichtigt Sie, wenn ein Benutzer mit der linken Maustaste auf die Diagrammlinie, die Histogrammleiste oder das Berichtselement doppelklickt.

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

Index des ausgewählten Indikators im [**Counters-Auflistungsobjekt.**](counters.md) Wenn kein Zähler ausgewählt wurde, wird der Indexwert 0 zurückgegeben. Andernfalls wird der Index des ausgewählten Leistungsindikators zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn dieses Ereignis ausgelöst wird, wird der Indikator, den der Benutzer im Liniendiagramm und Histogramm ausgewählt hat, auch im Legendenbereich ausgewählt. Dadurch kann der Benutzer des Systemmonitors leichter erkennen, welcher Leistungsindikator ausgewählt wird, wenn mehrere Indikatorwerte angezeigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





