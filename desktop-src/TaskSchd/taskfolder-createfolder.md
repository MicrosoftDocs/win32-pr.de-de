---
title: TaskFolder.CreateFolder-Methode
description: Erstellt für die Skripterstellung einen Ordner für verwandte Aufgaben.
ms.assetid: 4fdc96bc-8c85-4b36-b3ea-bad7a46c3d35
keywords:
- CreateFolder-Methode Taskplaner
- CreateFolder-Methode Taskplaner , TaskFolder-Objekt
- TaskFolder-Objekt Taskplaner , CreateFolder-Methode
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
ms.openlocfilehash: 93a873ef59ea9d099a7a739e5238c722f4b908fd
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387078"
---
# <a name="taskfoldercreatefolder-method"></a>TaskFolder.CreateFolder-Methode

Erstellt für die Skripterstellung einen Ordner für verwandte Aufgaben.

## <a name="syntax"></a>Syntax


```VB
ppFolder = .CreateFolder( _
  ByVal folderName, _
  ByVal sddl _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*folderName* \[ In\]
</dt> <dd>

Der Name, der zum Identifizieren des Ordners verwendet wird. Wenn "FolderName \\ SubFolder1 \\ SubFolder2" angegeben ist, wird die gesamte Ordnerstruktur erstellt, wenn die Ordner nicht vorhanden sind. Dieser Parameter kann ein relativer Pfad zur aktuellen [**TaskFolder-Instanz**](taskfolder.md) sein. Der Stammtaskordner wird mit einem umgekehrten Schrägstrich \\ () angegeben. Ein Beispiel für einen Taskordnerpfad im Stammtaskordner ist \\ MyTaskFolder. Das Zeichen "." kann nicht zum Angeben des aktuellen Aufgabenordners und des "."-Zeichens verwendet werden. -Zeichen können nicht verwendet werden, um den übergeordneten Aufgabenordner im Pfad anzugeben.

</dd> <dt>

*sddl* \[ In\]
</dt> <dd>

Der Sicherheitsdeskriptor, der dem Ordner zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein [**TaskFolder-Objekt,**](taskfolder.md) das den neuen Unterordner darstellt.

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

 

 





