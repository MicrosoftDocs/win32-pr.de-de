---
title: TaskFolder.GetFolder-Eigenschaft
description: Ruft für die Skripterstellung einen Ordner ab, der Aufgaben an einem angegebenen Speicherort enthält.
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- GetFolder-Eigenschaft Taskplaner
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
ms.openlocfilehash: 0c65b3f50cc5b8ab75bb041a61b36ad66bb35891
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387029"
---
# <a name="taskfoldergetfolder-property"></a>TaskFolder.GetFolder-Eigenschaft

Ruft für die Skripterstellung einen Ordner ab, der Aufgaben an einem angegebenen Speicherort enthält.

## <a name="syntax"></a>Syntax


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a>Eigenschaftswert

Der Pfad (Speicherort) zum Ordner. Verwenden Sie keinen umgekehrten Schrägstrich, der auf den Namen des letzten Ordners im Pfad folgt. Der Stammtaskordner wird mit einem umgekehrten Schrägstrich \\ () angegeben. Ein Beispiel für einen Taskordnerpfad im Stammtaskordner ist \\ MyTaskFolder. Das Zeichen "." kann nicht zum Angeben des aktuellen Aufgabenordners und des "."-Zeichens verwendet werden. -Zeichen können nicht verwendet werden, um den übergeordneten Aufgabenordner im Pfad anzugeben.

## <a name="error-codes"></a>Fehlercodes

Der Ordner am angegebenen Speicherort. Der Ordner ist ein [**TaskFolder-Objekt.**](taskfolder.md)

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





