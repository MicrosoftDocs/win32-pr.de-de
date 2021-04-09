---
title: Enumerator. atendovstream-Eigenschaft (WSManDisp. h)
description: Ruft einen booleschen Wert ab, der angibt, ob in der Auflistung weitere Elemente vorhanden sind.
ms.assetid: 5e80674a-7889-4753-b0dd-4d7b44eba00a
ms.tgt_platform: multiple
keywords:
- Atendotstream-Eigenschaft Windows-Remoteverwaltung
- Atendobstream-Eigenschaft Windows-Remoteverwaltung, Enumeratorobjekt
- EnumeratorobjektWindows-Remoteverwaltung, atendobstream-Eigenschaft
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
ms.openlocfilehash: 023798f6c868e434218dd1a4dbdf1928bf4526a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103266"
---
# <a name="enumeratoratendofstream-property"></a>Enumerator. atendovstream (Eigenschaft)

Ruft einen booleschen Wert ab, der angibt, ob in der Auflistung weitere Elemente vorhanden sind.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Enumerator.AtEndOfStream As BOOLEAN
```



## <a name="property-value"></a>Eigenschaftswert

<dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>**Fall**


</dt> <dd>

Es sind keine weiteren Elemente in der Auflistung.

</dd> <dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>**Alarm**


</dt> <dd>

Es sind weitere Elemente verfügbar.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie das [**Enumeratorobjekt**](enumerator.md) freigeben, nachdem Sie alle benötigten Daten erhalten haben, werden alle ausstehenden enumerationsanforderungen entfernt. Weitere Informationen finden Sie unter [auflisten oder Auflisten aller Instanzen einer Ressource](enumerating-or-listing-all-instances-of-a-resource.md).

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Beispiel werden Betriebssystem Instanzen aufgelistet. Beachten Sie, dass die Freigabe des Enumerationsobjekt alle ausstehenden enumerationsanforderungen bereinigt. Die DisplayOutput-Unterroutine formatiert die Datenausgabe auf die gleiche Weise wie das WinRM. cmd-Tool.


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
| Header<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerator**](enumerator.md)
</dt> <dt>

[Auflisten oder Auflisten aller Instanzen einer Ressource](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

 





