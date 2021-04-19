---
description: Verwenden Sie die Count-Eigenschaft des "errbemubjectset"-Objekts, um zu bestimmen, wie viele Elemente in einer Auflistung von "errbemubjectset" vorliegen. Diese Eigenschaft ist schreibgeschützt.
ms.assetid: ad3d1265-a11e-4962-b1f3-60092d2f79ef
ms.tgt_platform: multiple
title: Errbemubjectset. Count-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Count
- ISWbemObjectSet.Count
- ISWbemObjectSet.get_Count
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3154e22bbdbc75080ceebdf8b1eef602cf5c3be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352738"
---
# <a name="swbemobjectsetcount-property"></a>Errbemubjectset. Count-Eigenschaft

Verwenden Sie die **count** -Eigenschaft des " [**errbemubjectset**](swbemobjectset.md) "-Objekts, um zu bestimmen, wie viele Elemente in einer Auflistung von " **errbemubjectset** " vorliegen. Diese Eigenschaft ist schreibgeschützt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemObjectSet.Count As Integer
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Bei der Verwendung von count muss bei der Verwendung von "count" nicht darauf geachtet werden, dass die Anzahl der Elemente in einer Auflistung mit der Anzahl der Elemente übereinstimmt. Wenn Sie die Anzahl für eine Sammlung anfordern, kann WMI nicht sofort mit einer Zahl Antworten. Stattdessen muss Sie die Elemente wirklich zählen und die gesamte Auflistung auflisten. Für eine Auflistung, die relativ wenige Elemente enthält, z. b. Dienste, dauert diese Enumeration wahrscheinlich weniger als eine Sekunde. Das zählen der Anzahl von Ereignissen in einer Ereignisprotokoll Sammlung kann jedoch erheblich länger dauern.

Angenommen, Sie möchten die Eigenschaftswerte für jedes Ereignis in der Sammlung anzeigen. Wenn dies der Fall ist, muss WMI die gesamte Auflistung ein zweites Mal auflisten.

> [!Note]  
> Wenn Sie versuchen, diese Eigenschaft von einem von einer Methode zurückgegebenen " [**errbemubjectset**](swbemobjectset.md) "-Objekt zu erhalten, bei dem die angegebenen Flags das wbemFlagForwardOnly-Flag enthalten, erhalten Sie einen wbemErrFailed-Fehler.

 

## <a name="examples"></a>Beispiele

Der einzige Schritt, den Sie jemals mit einem "errbemubjectset" ausführen, ist das Auflisten aller Objekte, die in der Auflistung enthalten sind. Die Anzahl der Zähler, die bei der Skripterstellung für die System Administration nützlich sein können. Wie der Name schon sagt, gibt count die Anzahl der Elemente in der Auflistung an. Dieses Skript ruft z. b. eine Sammlung aller auf einem Computer installierten Dienste ab und gibt dann die Gesamtzahl der gefundenen Dienste wieder:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
Wscript.Echo "Services installed on target computer: " & colSWbemObjectSet.Count

```



Die Anzahl ist hilfreich, wenn Sie erkennen können, ob eine bestimmte Instanz auf einem Computer verfügbar ist. Dieses Skript ruft z. b. eine Sammlung aller Dienste auf einem Computer ab, die den Namen W3SVC haben. Wenn die Anzahl 0 beträgt (und es für Sammlungen zulässig ist, keine Instanzen zu haben), bedeutet dies, dass der W3SVC-Dienst nicht auf dem Computer installiert ist.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
    ("SELECT * FROM Win32_Service WHERE Name='w3svc'")
If colSWbemObjectSet.Count = 0 Then
    Wscript.Echo "W3SVC service is not installed on target computer."
Else
    For Each objSWbemObject In colSWbemObjectSet
        ' Perform task on World Wide Web Publishing service.
    Next
End If
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Objekt Satz<br/>                                                        |
| IID<br/>                      | IID \_ iswbemubjectset<br/>                                                         |



 

 




