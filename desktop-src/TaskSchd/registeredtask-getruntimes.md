---
title: Registeredtask. getruntimes-Methode
description: Ruft bei der Skripterstellung die Zeiten ab, zu denen die Ausführung der registrierten Aufgabe innerhalb eines angegebenen Zeitraums geplant ist.
ms.assetid: fc3d93eb-3186-419f-9f6f-7d54f8ade1ad
keywords:
- Getruntimes-Methode Taskplaner
- Getruntimes-Methode Taskplaner, registeredtask-Objekt
- Registeredtask-Objekt Taskplaner, getruntimes-Methode
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
ms.openlocfilehash: c15aba82c5515578a3c58a485e47718d09176483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518503"
---
# <a name="registeredtaskgetruntimes-method"></a>Registeredtask. getruntimes-Methode

Ruft bei der Skripterstellung die Zeiten ab, zu denen die Ausführung der registrierten Aufgabe innerhalb eines angegebenen Zeitraums geplant ist.

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

*Anfang* \[ in\]
</dt> <dd>

Die Startzeit für die Abfrage.

</dd> <dt>

*Ende* \[ in\]
</dt> <dd>

Die Endzeit für die Abfrage.

</dd> <dt>

*Anzahl* \[ vorgenommen\]
</dt> <dd>

Die Anzahl der geplanten Zeiten, zu denen der Task ausgeführt wird.

</dd> <dt>

*rgsttasktimes* \[ vorgenommen\]
</dt> <dd>

Die geplanten Zeiten, zu denen der Task ausgeführt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

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

 

 





