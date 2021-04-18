---
title: TaskService. GetFolder-Methode
description: Ruft bei der Skripterstellung einen Ordner registrierter Tasks ab.
ms.assetid: 57e5b411-1fb6-4ee1-9802-ed2adbb4fdf8
keywords:
- GetFolder-Methode Taskplaner
- GetFolder-Methode Taskplaner, Task Service-Objekt
- Task Service-Objekt Taskplaner, GetFolder-Methode
topic_type:
- apiref
api_name:
- TaskService.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74504e9cad124f8cbc9ec23e896ba4dec7d7f50c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341038"
---
# <a name="taskservicegetfolder-method"></a>TaskService. GetFolder-Methode

Ruft bei der Skripterstellung einen Ordner registrierter Tasks ab.

## <a name="syntax"></a>Syntax


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfad* \[ in\]
</dt> <dd>

Der Pfad zu dem Ordner, der abgerufen werden soll. Verwenden Sie keinen umgekehrten Schrägstrich nach dem letzten Ordnernamen im Pfad. Der Stamm Aufgaben Ordner wird mit einem umgekehrten Schrägstrich () angegeben \) . Ein Beispiel für einen Aufgaben Ordner Pfad unter dem Stamm Aufgaben Ordner ist \\ mytaskfolder. Das Zeichen "." kann nicht verwendet werden, um den aktuellen Aufgaben Ordner und ".." anzugeben. Zeichen können nicht verwendet werden, um den übergeordneten Aufgaben Ordner im Pfad anzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein [**taskfolder**](taskfolder.md) -Objekt für den angeforderten Ordner.

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

 

 





