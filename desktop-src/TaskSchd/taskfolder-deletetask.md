---
title: Taskfolder. DeleteTask-Methode
description: Löscht bei der Skripterstellung eine Aufgabe aus dem Ordner.
ms.assetid: c030b2bf-fbde-4b8b-b38b-763938855d12
keywords:
- DeleteTask-Methode Taskplaner
- DeleteTask-Methode Taskplaner, Task Folder-Objekt
- Task Folder-Objekt Taskplaner, DeleteTask-Methode
topic_type:
- apiref
api_name:
- TaskFolder.DeleteTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad4cf0a881a62cf5e9c1600653e5df58f3000f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742176"
---
# <a name="taskfolderdeletetask-method"></a>Taskfolder. DeleteTask-Methode

Löscht bei der Skripterstellung eine Aufgabe aus dem Ordner.

## <a name="syntax"></a>Syntax


```VB
TaskFolder.DeleteTask( _
  ByVal Name, _
  ByVal flags _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ in\]
</dt> <dd>

Der Name der Aufgabe, die beim Registrieren der Aufgabe angegeben wird. Das Zeichen "." kann nicht verwendet werden, um den aktuellen Aufgaben Ordner und ".." anzugeben. Zeichen können nicht verwendet werden, um den übergeordneten Aufgaben Ordner im Pfad anzugeben.

</dd> <dt>

*Flags* \[ in\]
</dt> <dd>

Wird nicht unterstützt. Der Wert ist 0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

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

 

 





