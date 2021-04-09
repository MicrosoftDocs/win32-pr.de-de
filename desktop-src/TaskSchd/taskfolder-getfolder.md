---
title: Taskfolder. GetFolder (Eigenschaft)
description: Ruft bei der Skripterstellung einen Ordner ab, der Tasks an einem angegebenen Speicherort enthält.
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- GetFolder-Eigenschaft Taskplaner
- GetFolder-Eigenschaft Taskplaner, Task Folder-Objekt
- Task Folder-Objekt Taskplaner, GetFolder-Eigenschaft
topic_type:
- apiref
api_name:
- TaskFolder.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 308173660ffff7d2062febd087c89cb63bcd8d99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103186"
---
# <a name="taskfoldergetfolder-property"></a>Taskfolder. GetFolder (Eigenschaft)

Ruft bei der Skripterstellung einen Ordner ab, der Tasks an einem angegebenen Speicherort enthält.

## <a name="syntax"></a>Syntax


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a>Eigenschaftswert

Der Pfad (Speicherort) zum Ordner. Verwenden Sie keinen umgekehrten Schrägstrich nach dem letzten Ordnernamen im Pfad. Der Stamm Aufgaben Ordner wird mit einem umgekehrten Schrägstrich () angegeben \) . Ein Beispiel für einen Aufgaben Ordner Pfad unter dem Stamm Aufgaben Ordner ist \\ mytaskfolder. Das Zeichen "." kann nicht verwendet werden, um den aktuellen Aufgaben Ordner und ".." anzugeben. Zeichen können nicht verwendet werden, um den übergeordneten Aufgaben Ordner im Pfad anzugeben.

## <a name="error-codes"></a>Fehlercodes

Der Ordner am angegebenen Speicherort. Der Ordner ist ein [**Task Folder**](taskfolder.md) -Objekt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





