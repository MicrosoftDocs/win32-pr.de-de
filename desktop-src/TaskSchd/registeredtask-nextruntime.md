---
title: RegisteredTask.NextRunTime (Eigenschaft)
description: Für die Skripterstellung wird der Zeitpunkt der nächsten geplanten Ausführung des registrierten Tasks ab.
ms.assetid: f63298a8-c9fa-4fea-ad0b-2c8739aced19
keywords:
- NextRunTime-Taskplaner
- NextRunTime-Eigenschaft Taskplaner , RegisteredTask-Objekt
- RegisteredTask-Objekt Taskplaner , NextRunTime-Eigenschaft
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
ms.openlocfilehash: 850c0215555fd24b729b1d71acaff9fa7083c0f53289f28e4228b8e57ff40e52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060048"
---
# <a name="registeredtasknextruntime-property"></a>RegisteredTask.NextRunTime (Eigenschaft)

Für die Skripterstellung wird der Zeitpunkt der nächsten geplanten Ausführung des registrierten Tasks ab.

## <a name="syntax"></a>Syntax


```VB
RegisteredTask.NextRunTime As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Zeit, zu der die nächste Ausführung des registrierten Task geplant ist.

## <a name="remarks"></a>Hinweise

Wenn der registrierte Task Trigger enthält, die einzeln deaktiviert sind, wirken sich diese Trigger weiterhin auf die nächste geplante Laufzeit aus, die zurückgegeben wird, obwohl sie deaktiviert sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





