---
description: Die Properties- \_ Eigenschaft des "errbemubject"-Objekts gibt ein "errbempropertyset"-Objekt zurück, das eine Auflistung der Eigenschaften für die aktuelle Klasse oder Instanz ist. Diese Eigenschaft ist schreibgeschützt.
ms.assetid: 8dd49678-47e7-4c6b-ab12-42532065eaf2
ms.tgt_platform: multiple
title: SWbemObject.Properties_-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Properties_
- ISWbemObject.Properties_
- ISWbemObject.get_Properties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b215abb7a0ca466c8a93fe20f20518f8d7b2ec8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348883"
---
# <a name="swbemobjectproperties_-property"></a>Errbemubject. Properties- \_ Eigenschaft

Die **Properties \_** -Eigenschaft des " [**errbemubject**](swbemobject.md) "-Objekts gibt ein " [**errbempropertyset**](swbempropertyset.md) "-Objekt zurück, das eine Auflistung der Eigenschaften für die aktuelle Klasse oder Instanz ist. Diese Eigenschaft ist schreibgeschützt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemObject.Properties_ As Object
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="examples"></a>Beispiele

Das PowerShell-Codebeispiel PowerShell- [WMI-Klassen Skripts generieren](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) in der TechNet Gallery verwendet die Properties \_ -Eigenschaft, um ein Skript für jede der WMI-Klassen zu generieren, die den WMI-Klassennamen und die Eigenschaften auflisten.

Der folgende Code, der aus der [Liste alle Eigenschaften für ein WMI-Klassen](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) -VBScript-Codebeispiel in der TechNet Gallery stammt, listet die Eigenschaften für eine angegebene WMI-Klasse auf.


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Properties" 
WScript.Echo "------------------------------" 
  
For Each objClassProperty In objClass.Properties_ 
    WScript.Echo objClassProperty.Name 
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
| CLSID<br/>                    | CLSID- \_ Austausch Objekt<br/>                                                           |
| IID<br/>                      | IID \_ iswbemujekt<br/>                                                            |



 

 




