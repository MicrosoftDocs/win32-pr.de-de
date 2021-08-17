---
title: RunningTask.EnginePID (Eigenschaft)
description: Für die Skripterstellung ruft die Prozess-ID für die Engine (den Prozess) ab, die die Aufgabe ausgeführt.
ms.assetid: cb8a0f2f-ebe3-4f52-8fbd-b0cebb539728
keywords:
- EnginePID-Taskplaner
- EnginePID-Eigenschaft Taskplaner , RunningTask-Objekt
- RunningTask-Taskplaner , EnginePID-Eigenschaft
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
ms.openlocfilehash: eed259ccc92e954ae1acde076f0cc09167d15071ea71a33039e7298479875b5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759073"
---
# <a name="runningtaskenginepid-property"></a>RunningTask.EnginePID (Eigenschaft)

Für die Skripterstellung ruft die Prozess-ID für die Engine (den Prozess) ab, die die Aufgabe ausgeführt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
RunningTask.EnginePID As Integer
```



## <a name="property-value"></a>Eigenschaftswert

Die Prozess-ID für die Engine, die den Task ausgeführt.

## <a name="remarks"></a>Hinweise

Die von dieser Eigenschaft zurückgegebene Prozess-ID kann nicht direkt an eine Zeichenfolge angefügt werden. Der zurückgegebene Wert muss zuerst durch Aufrufen der [CInt-Funktion](/previous-versions//fctcwhw9(v=vs.85)) für den zurückgegebenen Wert in einen ganzzahligen Wert konvertiert werden.


```VB
ProcessId = cint(RunningTask.EnginePID)
wscript.echo "Process Id of Engine is " & "ProcessId
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

