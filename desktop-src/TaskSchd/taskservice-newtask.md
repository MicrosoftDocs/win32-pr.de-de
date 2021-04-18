---
title: TaskService. newtask-Methode
description: Gibt für die Skripterstellung ein leeres Aufgaben Definitions Objekt zurück, das mit Einstellungen und Eigenschaften ausgefüllt und dann mithilfe der Task Folder. RegisterTaskDefinition-Methode registriert werden soll.
ms.assetid: 696d57fc-100a-43e6-a8d9-9ec89be40367
keywords:
- Newtask-Methode Taskplaner
- Newtask-Methode Taskplaner, Task Service-Objekt
- Task Service-Objekt Taskplaner, newtask-Methode
topic_type:
- apiref
api_name:
- TaskService.NewTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f5f10ce90861c76d0a751c54e8282269b7a8986
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345523"
---
# <a name="taskservicenewtask-method"></a>TaskService. newtask-Methode

Gibt für die Skripterstellung ein leeres Aufgaben Definitions Objekt zurück, das mit Einstellungen und Eigenschaften ausgefüllt und dann mithilfe der [**Task Folder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) -Methode registriert werden soll.

## <a name="syntax"></a>Syntax


```VB
TaskService.NewTask( _
  ByVal flags _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ in\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert und muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Aufgabendefinition, die alle zum Erstellen einer neuen Aufgabe erforderlichen Informationen angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





