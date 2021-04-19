---
title: Systemmonitor. oncounterselected-Ereignis
description: Benachrichtigt Sie, wenn ein Counter ausgewählt wird.
ms.assetid: 788a95a7-47ec-41f9-bf46-324ad3cc8a4e
keywords:
- Oncounterselected-Ereignis (Sysmon)
- Oncounterselected-Ereignis (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse "sysmon", oncounterselected-Ereignis
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterSelected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0174ab2f896a27e44df592ec28b7cb12a03198f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342439"
---
# <a name="systemmonitoroncounterselected-event"></a>Systemmonitor. oncounterselected-Ereignis

Benachrichtigt Sie, wenn ein Counter ausgewählt wird.

## <a name="syntax"></a>Syntax


```VB
SystemMonitor.OnCounterSelected( _
  ByVal index As Long _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

Index des ausgewählten Indikators im [**indikatorensammlungs Objekt**](counters.md) .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Sie können dieses Ereignis empfangen, wenn

-   Sie legen " [**count Item. Selected**](counteritem-selected.md) " auf "true" fest.
-   Der Benutzer wählt einen gegen Wert in der Legende aus.
-   Der Benutzer doppelklickt auf einen Gegenstand in der Legende.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Systemmonitor. oncounteradded**](systemmonitor-oncounteradded.md)
</dt> <dt>

[**Systemmonitor. oncounterdeleted**](-systemmonitor-oncounterdeleted.md)
</dt> </dl>

 

 





