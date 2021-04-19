---
title: Systemmonitor. oncounteradded-Ereignis
description: Benachrichtigt Sie, wenn der Zähler Sammlung ein Indikator hinzugefügt wird.
ms.assetid: f798443f-e2f1-4d25-b142-d88d6e4fe12c
keywords:
- Oncounteradded-Ereignis-sysmon
- Oncounteradded-Ereignis (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse sysmon, oncounteradded-Ereignis
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterAdded
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f150709114ae25da89b107c7de85e3c5eca2551f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342427"
---
# <a name="systemmonitoroncounteradded-event"></a>Systemmonitor. oncounteradded-Ereignis

Benachrichtigt Sie, wenn der [**Zähler**](counters.md) Sammlung ein Indikator hinzugefügt wird.

## <a name="syntax"></a>Syntax


```VB
SystemMonitor.OnCounterAdded( _
  ByVal index As Long _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

Index des Indikators [**, der dem indikatorensammlungs Objekt**](counters.md) hinzugefügt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Systemmonitor. oncounterdeleted**](-systemmonitor-oncounterdeleted.md)
</dt> <dt>

[**Systemmonitor. oncounterselected**](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





