---
title: Systemmonitor. oncounterdeleted-Ereignis
description: Benachrichtigt Sie, bevor ein Indikator aus der Zähler Sammlung gelöscht wird.
ms.assetid: ab6bc1ba-20cd-4774-853e-b6adb765fae3
keywords:
- Oncounterdeleted-Ereignis (Sysmon)
- Oncounterdeleted-Ereignis (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse "sysmon", oncounterdeleted-Ereignis
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
ms.openlocfilehash: ceafcc73f38e5413e312d00bf8aa8eba4eaf2c35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956521"
---
# <a name="systemmonitoroncounterdeleted-event"></a>Systemmonitor. oncounterdeleted-Ereignis

Benachrichtigt Sie, bevor ein Indikator aus der [**Zähler**](counters.md) Sammlung gelöscht wird.

## <a name="syntax"></a>Syntax


```VB
SystemMonitor.OnCounterDeleted( _
  ByVal index As Long _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

Index des Indikators [**, der aus**](counters.md) dem indikatorensammlungs Objekt gelöscht werden soll.

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

[**Systemmonitor. oncounteradded**](systemmonitor-oncounteradded.md)
</dt> <dt>

[**Systemmonitor. oncounterselected**](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





