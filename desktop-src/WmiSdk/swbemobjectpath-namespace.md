---
description: Die Namespace-Eigenschaft des SWbemObjectPath-Objekts enthält den Namen des Namespace, der Teil des Objektpfads ist.
ms.assetid: be88670d-6f0d-4b9d-886f-3e70bf4758ed
ms.tgt_platform: multiple
title: SWbemObjectPath.Namespace-Eigenschaft (Wbemdisp.h)
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
ms.openlocfilehash: f9daa9b74918c16d58546f6830bb474e40e449a8c596f61f7e27f03342c47b4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503760"
---
# <a name="swbemobjectpathnamespace-property"></a>SWbemObjectPath.Namespace-Eigenschaft

Die **Namespace-Eigenschaft** des [**SWbemObjectPath-Objekts**](swbemobjectpath.md) enthält den Namen des Namespace, der Teil des Objektpfads ist. Der folgende Pfad zeigt beispielsweise die Namespaceeigenschaft, die root \\ cimv2 zurückgibt:

``` syntax
\\computer\root\cimv2:win32_logicaldisk="a:"
```

Die Syntaxerklärung finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemObjectPath.Namespace As String
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie Sie den Namespacenamen von [**Win32 \_ LogicalDisk-Instanzen**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) abrufen, bei denen es sich um Festplatten handelt. Das Skript stellt eine Verbindung mit dem Standardnamespace herstellt.


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
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



 

