---
description: Die Properties-Eigenschaft des SWbemObject-Objekts gibt ein SWbemPropertySet-Objekt zurück, das eine Auflistung der Eigenschaften für die aktuelle Klasse oder \_ Instanz ist. Diese Eigenschaft ist schreibgeschützt.
ms.assetid: 8dd49678-47e7-4c6b-ab12-42532065eaf2
ms.tgt_platform: multiple
title: SWbemObject.Properties_ -Eigenschaft (Wbemdisp.h)
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
ms.openlocfilehash: 413e13b725fce117b9358a254a860c631fc5fbe3158bf7f6d277ebca22647168
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857310"
---
# <a name="swbemobjectproperties_-property"></a>SWbemObject.Properties(Eigenschaft) \_

Die **\_ Properties-Eigenschaft** des [**SWbemObject-Objekts**](swbemobject.md) gibt ein [**SWbemPropertySet-Objekt**](swbempropertyset.md) zurück, das eine Auflistung der Eigenschaften für die aktuelle Klasse oder Instanz ist. Diese Eigenschaft ist schreibgeschützt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemObject.Properties_ As Object
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="examples"></a>Beispiele

Das [PowerShell-Codebeispiel Generate PowerShell WMI Class Scripts](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) (PowerSHELL-WMI-Klassenskripts generieren) im TechNet-Katalog verwendet die Properties-Eigenschaft, um ein Skript für jede WMI-Klasse zu generieren, die den WMI-Klassennamen und die Eigenschaften \_ auflistet.

Der folgende Code, der aus dem VbScript-Codebeispiel List [All the Properties for a WMI Class](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) (Alle Eigenschaften für eine WMI-Klasse) im TechNet-Katalog übernommen wurde, listet die Eigenschaften für eine angegebene WMI-Klasse auf.


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
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




