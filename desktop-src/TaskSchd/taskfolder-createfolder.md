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
ms.openlocfilehash: 2a5de913ccf98ee8369430425e423813168c083cbde737b5831917a5ee594e1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759020"
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

Der Name, der zum Identifizieren des Ordners verwendet wird. Wenn "FolderName \\ SubFolder1 \\ SubFolder2" angegeben ist, wird die gesamte Ordnerstruktur erstellt, wenn die Ordner nicht vorhanden sind. Dieser Parameter kann ein relativer Pfad zur aktuellen [**TaskFolder-Instanz**](taskfolder.md) sein. Der Stammtaskordner wird mit einem umgekehrten Schrägstrich \\ () angegeben. Ein Beispiel für einen Taskordnerpfad im Stammtaskordner ist \\ MyTaskFolder. Das Zeichen "." kann nicht zum Angeben des aktuellen Aufgabenordners und des .-Zeichens verwendet werden. -Zeichen können nicht verwendet werden, um den übergeordneten Aufgabenordner im Pfad anzugeben.

</dd> <dt>

*sddl* \[ In\]
</dt> <dd>

Der Sicherheitsdeskriptor, der dem Ordner zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein [**TaskFolder-Objekt,**](taskfolder.md) das den neuen Unterordner darstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





