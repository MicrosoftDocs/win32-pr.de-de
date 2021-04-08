---
title: TaskService. highestversion (Eigenschaft)
description: Gibt für die Skripterstellung die höchste Version von Taskplaner an, die von einem Computer unterstützt wird.
ms.assetid: b4e55e46-6f33-4224-811b-06bf218dd1ac
keywords:
- Highestversion-Eigenschaft Taskplaner
- Highestversion-Eigenschaft Taskplaner, Task Service-Objekt
- TaskService-Objekt Taskplaner, highestversion-Eigenschaft
topic_type:
- apiref
api_name:
- TaskService.HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b4e381326ab901fcaf8657975ce3f8401facd44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743736"
---
# <a name="taskservicehighestversion-property"></a>TaskService. highestversion (Eigenschaft)

Gibt für die Skripterstellung die höchste Version von Taskplaner an, die von einem Computer unterstützt wird.

## <a name="syntax"></a>Syntax


```VB
TaskService.HighestVersion As Integer
```



## <a name="property-value"></a>Eigenschaftswert

Die höchste Version von Taskplaner, die ein Computer unterstützt. Die höchste Version ist ein Wert, der in MajorVersion/MinorVersion an der 16-Bit-Grenze aufgeteilt ist. Der Taskplaner-Dienst gibt 1 für die Hauptversion und 2 für die neben Version zurück. Verwenden Sie die [CLng](/previous-versions//ck4c5842(v=vs.85)) -Funktion, um den ganzzahligen Wert der Eigenschaft zu erhalten.

## <a name="examples"></a>Beispiele

Der folgende Code zeigt, wie die [CLng](/previous-versions//ck4c5842(v=vs.85)) -Funktion verwendet wird, um den Wert der **highestversion** -Eigenschaft zu erhalten.


```VB
wscript.echo service.HighestVersion
Test = clng( service.HighestVersion )
If Test <> 65538  Then
    wscript.echo "Fail"

Else
    wscript.echo "Pass"
End If
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

