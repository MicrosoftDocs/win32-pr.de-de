---
title: SystemMonitor.OnCounterDeleted-Ereignis
description: Benachrichtigt Sie, bevor ein Zähler aus der Counters-Auflistung gelöscht wird.
ms.assetid: ab6bc1ba-20cd-4774-853e-b6adb765fae3
keywords:
- OnCounterDeleted-Ereignis SysMon
- OnCounterDeleted-Ereignis SysMon , SystemMonitor-Klasse
- SystemMonitor-Klasse SysMon , OnCounterDeleted-Ereignis
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterDeleted
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44c178cb0b9c19fde0814f15729ffd49a0a0dbea65023bde06673cd843aeb668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884002"
---
# <a name="systemmonitoroncounterdeleted-event"></a>SystemMonitor.OnCounterDeleted-Ereignis

Benachrichtigt Sie, bevor ein Zähler aus der [**Counters-Auflistung gelöscht**](counters.md) wird.

## <a name="syntax"></a>Syntax


```VB
SystemMonitor.OnCounterDeleted( _
  ByVal index As Long _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

Index des Zählers, der aus dem [**Counters-Auflistungsobjekt**](counters.md) gelöscht werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemMonitor.OnCounterAdded**](systemmonitor-oncounteradded.md)
</dt> <dt>

[**SystemMonitor.OnCounterSelected**](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





