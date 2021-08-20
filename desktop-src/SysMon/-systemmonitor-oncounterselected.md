---
title: SystemMonitor.OnCounterSelected-Ereignis
description: Benachrichtigt Sie, wenn ein Leistungsindikator ausgewählt ist.
ms.assetid: 788a95a7-47ec-41f9-bf46-324ad3cc8a4e
keywords:
- OnCounterSelected-Ereignis SysMon
- OnCounterSelected-Ereignis SysMon , SystemMonitor-Klasse
- SystemMonitor-Klasse SysMon , OnCounterSelected-Ereignis
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
ms.openlocfilehash: 9e5e5402eb123c5edd44a5616b6973940ba065e2b0c8c2bfa63e7d151ae30124
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117957247"
---
# <a name="systemmonitoroncounterselected-event"></a>SystemMonitor.OnCounterSelected-Ereignis

Benachrichtigt Sie, wenn ein Leistungsindikator ausgewählt ist.

## <a name="syntax"></a>Syntax


```VB
SystemMonitor.OnCounterSelected( _
  ByVal index As Long _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

Index des ausgewählten Indikators im [**Counters-Auflistungsobjekt.**](counters.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Sie können dieses Ereignis empfangen, wenn

-   Legen Sie [**CounterItem.Selected auf**](counteritem-selected.md) TRUE fest.
-   Der Benutzer wählt einen Zähler in der Legende aus.
-   Der Benutzer doppelklickt in der Legende auf einen Zähler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SystemMonitor.OnCounterAdded**](systemmonitor-oncounteradded.md)
</dt> <dt>

[**SystemMonitor.OnCounterDeleted**](-systemmonitor-oncounterdeleted.md)
</dt> </dl>

 

 





