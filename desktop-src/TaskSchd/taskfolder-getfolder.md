---
title: TaskFolder.GetFolder (Eigenschaft)
description: Ruft für die Skripterstellung einen Ordner ab, der Aufgaben an einem angegebenen Speicherort enthält.
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- GetFolder-Taskplaner
- GetFolder-Eigenschaft Taskplaner , TaskFolder-Objekt
- TaskFolder-Objekt Taskplaner , GetFolder-Eigenschaft
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
ms.openlocfilehash: 7668b2486a316fe2bf799762401459ec7da2602ff52a4d5d3dc9ddb4dd888e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758983"
---
# <a name="taskfoldergetfolder-property"></a>TaskFolder.GetFolder (Eigenschaft)

Ruft für die Skripterstellung einen Ordner ab, der Aufgaben an einem angegebenen Speicherort enthält.

## <a name="syntax"></a>Syntax


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a>Eigenschaftswert

Der Pfad (Speicherort) zum Ordner. Verwenden Sie keinen zurücken Schrägstrich nach dem Namen des letzten Ordners im Pfad. Der Stammordner des Task wird mit einem schrägen Schrägstrich () \\ angegeben. Ein Beispiel für einen Taskordnerpfad unter dem Stammaufgabenordner ist \\ MyTaskFolder. Das Zeichen "." kann nicht verwendet werden, um den aktuellen Taskordner und den "." anzugeben. -Zeichen können nicht verwendet werden, um den übergeordneten Taskordner im Pfad anzugeben.

## <a name="error-codes"></a>Fehlercodes

Der Ordner am angegebenen Speicherort. Der Ordner ist ein [**TaskFolder-Objekt.**](taskfolder.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





