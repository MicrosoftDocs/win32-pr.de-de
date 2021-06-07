---
title: TaskService.GetFolder-Methode
description: Ruft für die Skripterstellung einen Ordner mit registrierten Tasks ab.
ms.assetid: 57e5b411-1fb6-4ee1-9802-ed2adbb4fdf8
keywords:
- GetFolder-Taskplaner
- GetFolder-Methode Taskplaner , TaskService-Objekt
- TaskService-Taskplaner , GetFolder-Methode
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
ms.openlocfilehash: 5e58f2d930a0577b6f1be620891b7ba631f18d77
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387099"
---
# <a name="taskservicegetfolder-method"></a>TaskService.GetFolder-Methode

Ruft für die Skripterstellung einen Ordner mit registrierten Tasks ab.

## <a name="syntax"></a>Syntax


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfad* \[ In\]
</dt> <dd>

Der Pfad zum abzurufenden Ordner. Verwenden Sie keinen zurücken Schrägstrich nach dem Namen des letzten Ordners im Pfad. Der Stammordner des Task wird mit einem schrägen Schrägstrich () \\ angegeben. Ein Beispiel für einen Taskordnerpfad unter dem Stammaufgabenordner ist \\ MyTaskFolder. Das Zeichen "." kann nicht verwendet werden, um den aktuellen Taskordner und "." anzugeben. -Zeichen können nicht verwendet werden, um den übergeordneten Taskordner im Pfad anzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein [**TaskFolder-Objekt**](taskfolder.md) für den angeforderten Ordner.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





