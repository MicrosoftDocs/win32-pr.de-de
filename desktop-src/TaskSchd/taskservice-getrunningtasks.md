---
title: TaskService. getrunningtasks-Methode
description: Ruft bei der Skripterstellung eine Auflistung von laufenden Tasks ab.
ms.assetid: bae3c035-a6b2-4ca5-970b-d4bc808068ad
keywords:
- Getrunningtasks-Methode Taskplaner
- Getrunningtasks-Methode Taskplaner, Task Service-Objekt
- Task Service-Objekt Taskplaner, getrunningtasks-Methode
topic_type:
- apiref
api_name:
- TaskService.GetRunningTasks
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec585b9ed46af9a283e337c8f200687c512cd36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743737"
---
# <a name="taskservicegetrunningtasks-method"></a>TaskService. getrunningtasks-Methode

Ruft bei der Skripterstellung eine Auflistung von laufenden Tasks ab.

> [!Note]  
> **TaskService. getrunningtasks** gibt nur eine Auflistung von ausgeführte Tasks zurück, die unter oder unterhalb des Sicherheits Kontexts eines Benutzers ausgeführt werden. Für Mitglieder der Gruppe "Administratoren" gibt **getrunningtasks** beispielsweise eine Sammlung aller ausgelaufenden Aufgaben zurück, aber für Mitglieder der Gruppe "Benutzer" gibt **getrunningtasks** nur eine Auflistung von Aufgaben zurück, die unter dem Sicherheitskontext der Benutzergruppe ausgeführt werden.

 

## <a name="syntax"></a>Syntax


```VB
TaskService.GetRunningTasks( _
  ByVal flags _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ in\]
</dt> <dd>

Übergeben Sie 1, um alle laufenden Tasks, einschließlich ausgeblendeter Tasks, zurückzugeben. Übergeben Sie 0, um eine Auflistung von Aufgaben zurückzugeben, die keine ausgeblendeten Tasks sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein [**runningtaskcollection**](runningtaskcollection.md) -Objekt, das die derzeit laufenden Tasks enthält.

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
</dt> </dl>

 

 





