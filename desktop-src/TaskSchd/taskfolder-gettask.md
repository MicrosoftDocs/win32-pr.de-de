---
title: Taskfolder. gettask-Eigenschaft
description: Ruft bei der Skripterstellung eine Aufgabe an einer angegebenen Position in einem Ordner ab.
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- Gettask-Eigenschaft Taskplaner
- Gettask-Eigenschaft Taskplaner, taskfolder-Objekt
- Task Folder-Objekt Taskplaner, gettask-Eigenschaft
topic_type:
- apiref
api_name:
- TaskFolder.GetTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e813538cfcb995949cbe1fb8ec6a3b0d7772061c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740600"
---
# <a name="taskfoldergettask-property"></a>Taskfolder. gettask-Eigenschaft

Ruft bei der Skripterstellung eine Aufgabe an einer angegebenen Position in einem Ordner ab.

## <a name="syntax"></a>Syntax


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a>Eigenschaftswert

Der Pfad (Speicherort) für die Aufgabe in einem Ordner. Der Stamm Aufgaben Ordner wird mit einem umgekehrten Schrägstrich () angegeben \) . Ein Beispiel für einen Aufgaben Ordner Pfad unter dem Stamm Aufgaben Ordner ist \\ mytaskfolder. Das Zeichen "." kann nicht verwendet werden, um den aktuellen Aufgaben Ordner und ".." anzugeben. Zeichen können nicht verwendet werden, um den übergeordneten Aufgaben Ordner im Pfad anzugeben.

## <a name="error-codes"></a>Fehlercodes

Die Aufgabe an der angegebenen Position. Der Task ist ein [**registeredtask**](registeredtask.md) -Objekt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





