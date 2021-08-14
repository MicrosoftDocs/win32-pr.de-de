---
title: TaskFolder.GetTask (Eigenschaft)
description: Für die Skripterstellung ruft eine Aufgabe an einem angegebenen Speicherort in einem Ordner ab.
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- GetTask-Taskplaner
- GetTask-Eigenschaft Taskplaner , TaskFolder-Objekt
- TaskFolder-Objekt Taskplaner , GetTask-Eigenschaft
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
ms.openlocfilehash: 8369c09ad62329fa583bfba1cf718a3543c565f3e3d41f1d20f88339e37c44ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253420"
---
# <a name="taskfoldergettask-property"></a>TaskFolder.GetTask (Eigenschaft)

Für die Skripterstellung ruft eine Aufgabe an einem angegebenen Speicherort in einem Ordner ab.

## <a name="syntax"></a>Syntax


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a>Eigenschaftswert

Der Pfad (Speicherort) zur Aufgabe in einem Ordner. Der Stammordner des Task wird mit einem schrägen Schrägstrich () \\ angegeben. Ein Beispiel für einen Taskordnerpfad unter dem Stammaufgabenordner ist \\ MyTaskFolder. Das Zeichen "." kann nicht verwendet werden, um den aktuellen Taskordner und "." anzugeben. -Zeichen können nicht verwendet werden, um den übergeordneten Taskordner im Pfad anzugeben.

## <a name="error-codes"></a>Fehlercodes

Die Aufgabe am angegebenen Speicherort. Die Aufgabe ist ein [**RegisteredTask-Objekt.**](registeredtask.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





