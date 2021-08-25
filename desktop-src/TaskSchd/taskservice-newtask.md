---
title: TaskService.NewTask-Methode
description: Für die Skripterstellung gibt ein leeres Aufgabendefinitionsobjekt zurück, das mit Einstellungen und Eigenschaften ausgefüllt und dann mithilfe der TaskFolder.RegisterTaskDefinition-Methode registriert werden soll.
ms.assetid: 696d57fc-100a-43e6-a8d9-9ec89be40367
keywords:
- NewTask-Taskplaner
- NewTask-Methode Taskplaner , TaskService-Objekt
- TaskService-Taskplaner , NewTask-Methode
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
ms.openlocfilehash: e22da6f62f59bf24ded0eed9dea21e3a1a9d1c3e7ecc36fb6f425f58124aee71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990930"
---
# <a name="taskservicenewtask-method"></a>TaskService.NewTask-Methode

Für die Skripterstellung gibt ein leeres Aufgabendefinitionsobjekt zurück, das mit Einstellungen und Eigenschaften ausgefüllt und dann mithilfe der [**TaskFolder.RegisterTaskDefinition-Methode registriert werden**](taskfolder-registertaskdefinition.md) soll.

## <a name="syntax"></a>Syntax


```VB
TaskService.NewTask( _
  ByVal flags _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert und muss auf 0 festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Aufgabendefinition, die alle Informationen angibt, die zum Erstellen einer neuen Aufgabe erforderlich sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





