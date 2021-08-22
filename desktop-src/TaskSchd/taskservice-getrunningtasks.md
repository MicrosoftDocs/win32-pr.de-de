---
title: TaskService.GetRunningTasks-Methode
description: Ruft für die Skripterstellung eine Auflistung ausgeführter Aufgaben ab.
ms.assetid: bae3c035-a6b2-4ca5-970b-d4bc808068ad
keywords:
- GetRunningTasks-Taskplaner
- GetRunningTasks-Methode Taskplaner , TaskService-Objekt
- TaskService-Taskplaner , GetRunningTasks-Methode
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
ms.openlocfilehash: 9ecbc52451a4ed3dcc5f3ecc9984009e94dd9bf18b4c8dc667c0b040c43cc68c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072420"
---
# <a name="taskservicegetrunningtasks-method"></a>TaskService.GetRunningTasks-Methode

Ruft für die Skripterstellung eine Auflistung ausgeführter Aufgaben ab.

> [!Note]  
> **TaskService.GetRunningTasks gibt** nur eine Sammlung ausgeführter Aufgaben zurück, die im oder unter dem Sicherheitskontext eines Benutzers ausgeführt werden. Beispielsweise gibt **GetRunningTasks** für Mitglieder der Gruppe Administratoren eine Sammlung aller ausgeführten Aufgaben zurück. Für Mitglieder der Gruppe Benutzer gibt **GetRunningTasks** jedoch nur eine Sammlung von Aufgaben zurück, die im Sicherheitskontext der Gruppe Benutzer ausgeführt werden.

 

## <a name="syntax"></a>Syntax


```VB
TaskService.GetRunningTasks( _
  ByVal flags _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ In\]
</dt> <dd>

Übergeben Sie 1, um alle ausgeführten Aufgaben, einschließlich ausgeblendeter Aufgaben, zurück zu geben. Übergeben Sie 0, um eine Auflistung ausgeführter Aufgaben zurück zu geben, die keine ausgeblendeten Aufgaben sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein [**RunningTaskCollection-Objekt,**](runningtaskcollection.md) das die derzeit ausgeführten Aufgaben enthält.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





