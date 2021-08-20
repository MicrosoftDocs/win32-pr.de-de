---
title: Enumerator.AtEndOfStream-Eigenschaft (WSManDisp.h)
description: Ruft einen booleschen Wert ab, der angibt, ob die Auflistung weitere Elemente enthält.
ms.assetid: 5e80674a-7889-4753-b0dd-4d7b44eba00a
ms.tgt_platform: multiple
keywords:
- AtEndOfStream-Eigenschaft Windows Remoteverwaltung
- AtEndOfStream-Eigenschaft Windows Remoteverwaltung , Enumeratorobjekt
- Enumeratorobjekt Windows Remoteverwaltung , AtEndOfStream-Eigenschaft
topic_type:
- apiref
api_name:
- Enumerator.AtEndOfStream
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1077837f82d650b57dfea0316ef15094b18749eefdb6957e62e6afd92cfe672
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113201"
---
# <a name="enumeratoratendofstream-property"></a>Enumerator.AtEndOfStream-Eigenschaft

Ruft einen booleschen Wert ab, der angibt, ob die Auflistung weitere Elemente enthält.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Enumerator.AtEndOfStream As BOOLEAN
```



## <a name="property-value"></a>Eigenschaftswert

<dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>**STIMMT**


</dt> <dd>

In der Auflistung sind keine Elemente mehr enthalten.

</dd> <dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>**FALSE**


</dt> <dd>

Weitere Elemente sind verfügbar.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn Sie das [**Enumeratorobjekt**](enumerator.md) frei geben, nachdem Sie alle erforderlichen Daten abgerufen haben, werden alle ausstehenden Enumerationsanforderungen entfernt. Weitere Informationen finden Sie unter Auflisten oder Auflisten aller Instanzen [einer Ressource.](enumerating-or-listing-all-instances-of-a-resource.md)

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Beispiel werden Betriebssysteminstanzen aufzählt. Beachten Sie, dass durch die Freiung des Enumerationsobjekts alle ausstehenden Enumerationsanforderungen bereinigt werden. Die DisplayOutput-Unterroutine formatiert die Datenausgabe auf die gleiche Weise wie das WinRM.cmd-Tool.


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & _
    RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
    "wmi/root/cimv2/Win32_OperatingSystem"

Set objResultSet = objSession.Enumerate( strResource )

While Not objResultSet.AtEndOfStream
 
 DisplayOutput( objResultSet.ReadItem ) 

Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
 Dim xmlFile, xslFile
 Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
 Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
 xmlFile.LoadXml( strWinRMXml )
 xslFile.Load( "WsmTxt.xsl" )
 Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerator**](enumerator.md)
</dt> <dt>

[Auflisten oder Auflisten aller Instanzen einer Ressource](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

 





