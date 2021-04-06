---
title: Registeredtask. NextRunTime (Eigenschaft)
description: Ruft bei der Skripterstellung die Uhrzeit ab, zu der der registrierte Task die nächste geplante Ausführung ist.
ms.assetid: f63298a8-c9fa-4fea-ad0b-2c8739aced19
keywords:
- NextRunTime-Eigenschaft Taskplaner
- NextRunTime-Eigenschaft Taskplaner, registeredtask-Objekt
- Registeredtask-Objekt Taskplaner, NextRunTime-Eigenschaft
topic_type:
- apiref
api_name:
- RegisteredTask.NextRunTime
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94db26c023ddd2c146586fbc433548517a84f234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742777"
---
# <a name="registeredtasknextruntime-property"></a>Registeredtask. NextRunTime (Eigenschaft)

Ruft bei der Skripterstellung die Uhrzeit ab, zu der der registrierte Task die nächste geplante Ausführung ist.

## <a name="syntax"></a>Syntax


```VB
RegisteredTask.NextRunTime As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Zeitpunkt der nächsten geplanten Ausführung der registrierten Aufgabe.

## <a name="remarks"></a>Bemerkungen

Wenn die registrierte Aufgabe einzeln deaktivierte Trigger enthält, wirken sich diese Trigger weiterhin auf die nächste geplante Laufzeit aus, die zurückgegeben wird, auch wenn Sie deaktiviert sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**Registeredtask**](registeredtask.md)
</dt> </dl>

 

 





