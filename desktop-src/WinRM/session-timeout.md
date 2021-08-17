---
title: Session.Timeout-Eigenschaft (WSManDisp.h)
description: Legt die maximale Zeit in Millisekunden fest, die die Clientanwendung auf Windows Remoteverwaltung wartet, um ihre Vorgänge abzuschließen, und ruft sie ab.
ms.assetid: ca35722a-1fd3-48bf-a11b-4624cb81aae3
ms.tgt_platform: multiple
keywords:
- Timeouteigenschaft Windows Remoteverwaltung
- Timeouteigenschaft Windows Remoteverwaltung, Sitzungsobjekt
- Sitzungsobjekt Windows Remoteverwaltung, Timeout-Eigenschaft
topic_type:
- apiref
api_name:
- Session.Timeout
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4731e4f76ee890bc925a14b69c8ffb3d50e47406939b76183359021242a5fadc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743241"
---
# <a name="sessiontimeout-property"></a>Session.Timeout-Eigenschaft

Legt die maximale Zeit in Millisekunden fest, die die Clientanwendung auf Windows Remoteverwaltung wartet, um ihre Vorgänge abzuschließen, und ruft sie ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Session.Timeout As long
```



## <a name="property-value"></a>Eigenschaftswert

Time out-Wert in Millisekunden. Wenn der Time out-Wert überschritten wird, tritt ein Laufzeitfehler auf.

## <a name="remarks"></a>Hinweise

Der Time out-Wert kann vor jedem vom Agent ausgeführten Vorgang festgelegt werden. Wenn kein Time out-Wert angegeben wird, legt der Agent den Time out-Wert fest.

Während eines Enumerationsvorgangs kann der Time out-Wert nicht zurückgesetzt werden, während die Ressource aufzählt wird.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird ein Calc.exe Prozess mit der [**Create-Methode**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) der WMI [**Win32 \_ Process-Klasse**](/windows/desktop/CIMWin32Prov/win32-process) gestartet. Der *parameter strInputParameters* enthält die Eingabeparameter im XML-Format. Das Skript gibt ein Time out für die Sitzung an.


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
    "wmi/root/cimv2/Win32_Process"

'Reset timeout to 10,000 milliseconds
objSession.Timeout = 10000     

strInputParameters = "<p:Create_INPUT " & _
    "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Process"">" & _
    "<p:CommandLine>" & "calc.exe" & _
    "</p:CommandLine>" & _
    "</p:Create_INPUT>"

strOutputParameters = objSession.Invoke( "Create", _
    strResource, strInputParameters )

DisplayOutput( strOutputParameters )

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Sitzungskonsistenz**](session.md)
</dt> </dl>

 

