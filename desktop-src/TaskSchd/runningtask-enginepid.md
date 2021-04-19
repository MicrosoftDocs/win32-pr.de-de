---
title: Runningtask. enginepid (Eigenschaft)
description: Ruft bei der Skripterstellung die Prozess-ID für die Engine (Prozess) ab, die die Aufgabe ausführen soll.
ms.assetid: cb8a0f2f-ebe3-4f52-8fbd-b0cebb539728
keywords:
- Enginepid-Eigenschaft Taskplaner
- Enginepid-Eigenschaft Taskplaner, runningtask-Objekt
- Runningtask-Objekt Taskplaner, enginepid-Eigenschaft
topic_type:
- apiref
api_name:
- RunningTask.EnginePID
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd725c44fc85e82d3693d9467956d3040aad2bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339166"
---
# <a name="runningtaskenginepid-property"></a>Runningtask. enginepid (Eigenschaft)

Ruft bei der Skripterstellung die Prozess-ID für die Engine (Prozess) ab, die die Aufgabe ausführen soll.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
RunningTask.EnginePID As Integer
```



## <a name="property-value"></a>Eigenschaftswert

Die Prozess-ID für die Engine, die die Aufgabe ausführen soll.

## <a name="remarks"></a>Bemerkungen

Die von dieser Eigenschaft zurückgegebene Prozess-ID kann nicht direkt an eine Zeichenfolge angehängt werden. Der zurückgegebene Wert muss zuerst in einen ganzzahligen Wert konvertiert werden, indem die [CInt](/previous-versions//fctcwhw9(v=vs.85)) -Funktion für den zurückgegebenen Wert aufgerufen wird.


```VB
ProcessId = cint(RunningTask.EnginePID)
wscript.echo "Process Id of Engine is " & "ProcessId
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

