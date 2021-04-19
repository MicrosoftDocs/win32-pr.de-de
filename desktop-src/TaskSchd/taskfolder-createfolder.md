---
title: Taskfolder. kreatefolder-Methode
description: Erstellt bei der Skripterstellung einen Ordner für Verwandte Aufgaben.
ms.assetid: 4fdc96bc-8c85-4b36-b3ea-bad7a46c3d35
keywords:
- Taskplaner der Methode "kreatefolder"
- Methode der Methode "Taskplaner", "taskfolder"-Objekt
- Task Folder-Objekt Taskplaner, Methode "kreatefolder"
topic_type:
- apiref
api_name:
- TaskFolder.CreateFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ae66dadb0c943b1ca33be3e696ac1c8ca7d6234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341812"
---
# <a name="taskfoldercreatefolder-method"></a>Taskfolder. kreatefolder-Methode

Erstellt bei der Skripterstellung einen Ordner für Verwandte Aufgaben.

## <a name="syntax"></a>Syntax


```VB
ppFolder = .CreateFolder( _
  ByVal folderName, _
  ByVal sddl _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FolderName* \[ in\]
</dt> <dd>

Der Name, der zum Identifizieren des Ordners verwendet wird. Wenn "FolderName \\ Unterordner1 \\ SubFolder2" angegeben wird, wird die gesamte Ordnerstruktur erstellt, wenn die Ordner nicht vorhanden sind. Dieser Parameter kann ein relativer Pfad zur aktuellen [**Task Folder**](taskfolder.md) -Instanz sein. Der Stamm Aufgaben Ordner wird mit einem umgekehrten Schrägstrich () angegeben \) . Ein Beispiel für einen Aufgaben Ordner Pfad unter dem Stamm Aufgaben Ordner ist \\ mytaskfolder. Das Zeichen "." kann nicht verwendet werden, um den aktuellen Aufgaben Ordner und ".." anzugeben. Zeichen können nicht verwendet werden, um den übergeordneten Aufgaben Ordner im Pfad anzugeben.

</dd> <dt>

*SDDL* \[ in\]
</dt> <dd>

Die Sicherheits Beschreibung, die dem Ordner zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein [**taskfolder**](taskfolder.md) -Objekt, das den neuen Unterordner darstellt.

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

 

 





