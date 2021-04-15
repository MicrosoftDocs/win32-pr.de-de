---
title: Taskfolder. DeleteFolder-Methode
description: Bei der Skripterstellung wird ein Unterordner aus dem übergeordneten Ordner gelöscht.
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- DeleteFolder-Methode Taskplaner
- DeleteFolder-Methode Taskplaner, Task Folder-Objekt
- Task Folder-Objekt Taskplaner, DeleteFolder-Methode
topic_type:
- apiref
api_name:
- TaskFolder.DeleteFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea9b8aaa7da7710cedc49e10d6be2a203f62b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477481"
---
# <a name="taskfolderdeletefolder-method"></a>Taskfolder. DeleteFolder-Methode

Bei der Skripterstellung wird ein Unterordner aus dem übergeordneten Ordner gelöscht.

## <a name="syntax"></a>Syntax


```VB
TaskFolder.DeleteFolder( _
  ByVal folderName, _
  ByVal flags _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FolderName* \[ in\]
</dt> <dd>

Der Name des unter Ordners, der entfernt werden soll. Der Stamm Aufgaben Ordner wird mit einem umgekehrten Schrägstrich () angegeben \) . Dieser Parameter kann ein relativer Pfad zu dem Ordner sein, den Sie löschen möchten. Ein Beispiel für einen Aufgaben Ordner Pfad unter dem Stamm Aufgaben Ordner ist \\ mytaskfolder. Das Zeichen "." kann nicht verwendet werden, um den aktuellen Aufgaben Ordner und ".." anzugeben. Zeichen können nicht verwendet werden, um den übergeordneten Aufgaben Ordner im Pfad anzugeben.

</dd> <dt>

*Flags* \[ in\]
</dt> <dd>

Wird nicht unterstützt.

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

[**Task Folder**](taskfolder.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





