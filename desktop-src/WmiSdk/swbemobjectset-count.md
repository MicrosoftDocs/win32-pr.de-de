---
description: Verwenden Sie die Count-Eigenschaft des SWbemObjectSet-Objekts, um zu bestimmen, wie viele Elemente in einer SWbemObjectSet-Auflistung enthalten sind. Diese Eigenschaft ist schreibgeschützt.
ms.assetid: ad3d1265-a11e-4962-b1f3-60092d2f79ef
ms.tgt_platform: multiple
title: SWbemObjectSet.Count-Eigenschaft (Wbemdisp.h)
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
ms.openlocfilehash: c1305cc0119f002f8ac3229664227d5c21bea9d865eedb0a31fcb7eb77250424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857230"
---
# <a name="swbemobjectsetcount-property"></a>SWbemObjectSet.Count-Eigenschaft

Verwenden Sie die **Count-Eigenschaft** des [**SWbemObjectSet-Objekts,**](swbemobjectset.md) um zu bestimmen, wie viele Elemente in einer **SWbemObjectSet-Auflistung** enthalten sind. Diese Eigenschaft ist schreibgeschützt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemObjectSet.Count As Integer
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Wenn Sie Count verwenden, müssen Sie darauf achten, dass WMI nicht die Anzahl der Elemente in einer Auflistung aktiv hält. Wenn Sie Anzahl für eine Sammlung anfordern, kann WMI nicht sofort mit einer Zahl antworten. Stattdessen muss er die Elemente wörtlich zählen und die gesamte Auflistung aufzählen. Für eine Auflistung mit relativ wenigen Elementen, z. B. Diensten, dauert diese Enumeration wahrscheinlich weniger als eine Sekunde. Das Zählen der Anzahl von Ereignissen in einer Ereignisprotokollsammlung kann jedoch erheblich länger dauern.

Angenommen, Sie möchten die Eigenschaftswerte für jedes Ereignis in der Auflistung anzeigen. In diesem Falle muss WMI die gesamte Sammlung ein zweites Mal aufzählen.

> [!Note]  
> Wenn Sie versuchen, diese Eigenschaft aus einem [**SWbemObjectSet-Objekt**](swbemobjectset.md) abzurufen, das von einer Methode zurückgegeben wird, in der die angegebenen Flags das Flag wbemFlagForwardOnly enthalten, erhalten Sie einen wbemErrFailed-Fehler.

 

## <a name="examples"></a>Beispiele

In den meisten Teilen werden Sie mit einem SWbemObjectSet nur alle Objekte auflisten, die in der Auflistung selbst enthalten sind. Die Anzahl der Zähler, die bei der Skripterstellung für die Systemverwaltung nützlich sein kann. Wie der Name schon sagt, gibt Count die Anzahl der Elemente in der Auflistung an. Dieses Skript ruft z. B. eine Sammlung aller auf einem Computer installierten Dienste ab und gibt dann die Gesamtzahl der gefundenen Dienste wieder:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
Wscript.Echo "Services installed on target computer: " & colSWbemObjectSet.Count

```



Dies macht Count nützlich, da sie Ihnen mitteilen kann, ob eine bestimmte Instanz auf einem Computer verfügbar ist. Dieses Skript ruft beispielsweise eine Auflistung aller Dienste auf einem Computer mit dem Namen W3SVC ab. Wenn count gleich 0 (und für Sammlungen ohne Instanzen gültig) ist, bedeutet dies, dass der W3SVC-Dienst nicht auf dem Computer installiert ist.


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
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemObjectSet<br/>                                                         |



 

 




