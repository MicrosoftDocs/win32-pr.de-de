---
title: RegisteredTask.GetRunTimes-Methode
description: Ruft für die Skripterstellung die Zeiten ab, zu denen die Ausführung des registrierten Tasks während eines angegebenen Zeitraums geplant ist.
ms.assetid: fc3d93eb-3186-419f-9f6f-7d54f8ade1ad
keywords:
- GetRunTimes-Methode Taskplaner
- GetRunTimes-Methode Taskplaner , RegisteredTask-Objekt
- RegisteredTask-Objekt Taskplaner , GetRunTimes-Methode
topic_type:
- apiref
api_name:
- RegisteredTask.GetRunTimes
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303dd08c576f31946207241b086fe945b3f1ac275c596496139d19f507670e30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759665"
---
# <a name="registeredtaskgetruntimes-method"></a>RegisteredTask.GetRunTimes-Methode

Ruft für die Skripterstellung die Zeiten ab, zu denen die Ausführung des registrierten Tasks während eines angegebenen Zeitraums geplant ist.

## <a name="syntax"></a>Syntax


```VB
RegisteredTask.GetRunTimes( _
  ByVal begin, _
  ByVal end, _
  ByRef count, _
  ByRef rgstTaskTimes _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*begin* \[ In\]
</dt> <dd>

Die Startzeit für die Abfrage.

</dd> <dt>

*ende* \[ In\]
</dt> <dd>

Die Endzeit für die Abfrage.

</dd> <dt>

*count* \[ out\]
</dt> <dd>

Die Anzahl geplanter Ausführungszeiten des Tasks.

</dd> <dt>

*rgstTaskTimes* \[ out\]
</dt> <dd>

Die geplanten Zeiten, zu denen der Task ausgeführt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn der registrierte Task Trigger enthält, die einzeln deaktiviert sind, wirken sich diese Trigger weiterhin auf die nächste geplante Laufzeit aus, die zurückgegeben wird, obwohl sie deaktiviert sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





