---
description: Die Namespace-Eigenschaft des "errbemubjectpath"-Objekts enthält den Namen des Namespace, der Teil des Objekt Pfads ist.
ms.assetid: be88670d-6f0d-4b9d-886f-3e70bf4758ed
ms.tgt_platform: multiple
title: Errbemubjectpath. Namespace-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Namespace
- ISWbemObjectPath.Namespace
- ISWbemObjectPath.get_Namespace
- ISWbemObjectPath.put_Namespace
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 885f7069e901d1d4a490ad7539077463f6c1838c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216517"
---
# <a name="swbemobjectpathnamespace-property"></a>Errbemubjectpath. Namespace-Eigenschaft

Die **Namespace** -Eigenschaft des " [**errbemubjectpath**](swbemobjectpath.md) "-Objekts enthält den Namen des Namespace, der Teil des Objekt Pfads ist. Der folgende Pfad zeigt z. b. die Namespace-Eigenschaft, die root cimv2 zurückgibt \\ :

``` syntax
\\computer\root\cimv2:win32_logicaldisk="a:"
```

Die Syntax Erklärung finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemObjectPath.Namespace As String
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie Sie den Namespace Namen aus Instanzen von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) abrufen, bei denen es sich um Festplatten handelt. Das Skript stellt eine Verbindung mit dem Standard Namespace her.


```VB
Const HARD_DISK = 3
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer)

Set colDisks = objWMIService.ExecQuery _
    ("Select * from Win32_LogicalDisk " _
    & "Where DriveType = " & HARD_DISK & "")
For Each objDisk in colDisks
    Set objpath = objDisk.path_
    Wscript.Echo "Path of Win32_Logical disk instance " _
    & objDisk.DeviceID & " = " & objpath.Namespace   
Next
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Austausch Pfad<br/>                                                       |
| IID<br/>                      | IID \_ iswbemubjectpath<br/>                                                        |



 

