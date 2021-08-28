---
title: TaskService.GetFolder-Methode
description: Ruft für die Skripterstellung einen Ordner mit registrierten Aufgaben ab.
ms.assetid: 57e5b411-1fb6-4ee1-9802-ed2adbb4fdf8
keywords:
- GetFolder-Methode Taskplaner
- GetFolder-Methode Taskplaner , TaskService-Objekt
- TaskService-Objekt Taskplaner , GetFolder-Methode
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
ms.openlocfilehash: 632595e462abd5d6bba5c2e91ebcd590f4ec9a7289092eaf56626e4586691be3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072430"
---
# <a name="taskservicegetfolder-method"></a>TaskService.GetFolder-Methode

Ruft für die Skripterstellung einen Ordner mit registrierten Aufgaben ab.

## <a name="syntax"></a>Syntax


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Path (Pfad)* \[ In\]
</dt> <dd>

Der Pfad zum abzurufenden Ordner. Verwenden Sie keinen umgekehrten Schrägstrich, der auf den Namen des letzten Ordners im Pfad folgt. Der Stammtaskordner wird mit einem umgekehrten Schrägstrich \\ () angegeben. Ein Beispiel für einen Taskordnerpfad im Stammtaskordner ist \\ MyTaskFolder. Das Zeichen "." kann nicht zum Angeben des aktuellen Aufgabenordners und des .-Zeichens verwendet werden. -Zeichen können nicht verwendet werden, um den übergeordneten Aufgabenordner im Pfad anzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein [**TaskFolder-Objekt**](taskfolder.md) für den angeforderten Ordner.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





