---
title: TaskFolder.GetTask-Eigenschaft
description: Ruft für die Skripterstellung eine Aufgabe an einem angegebenen Speicherort in einem Ordner ab.
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- GetTask-Eigenschaft Taskplaner
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
ms.openlocfilehash: b697b8fa2d0715dcf0282c5f32490bfccec79fec
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387676"
---
# <a name="taskfoldergettask-property"></a>TaskFolder.GetTask-Eigenschaft

Ruft für die Skripterstellung eine Aufgabe an einem angegebenen Speicherort in einem Ordner ab.

## <a name="syntax"></a>Syntax


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a>Eigenschaftswert

Der Pfad (Speicherort) der Aufgabe in einem Ordner. Der Stammtaskordner wird mit einem umgekehrten Schrägstrich \\ () angegeben. Ein Beispiel für einen Taskordnerpfad im Stammtaskordner ist \\ MyTaskFolder. Das Zeichen "." kann nicht zum Angeben des aktuellen Aufgabenordners und des "."-Zeichens verwendet werden. -Zeichen können nicht verwendet werden, um den übergeordneten Aufgabenordner im Pfad anzugeben.

## <a name="error-codes"></a>Fehlercodes

Die Aufgabe an der angegebenen Position. Der Task ist ein [**RegisteredTask-Objekt.**](registeredtask.md)

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





