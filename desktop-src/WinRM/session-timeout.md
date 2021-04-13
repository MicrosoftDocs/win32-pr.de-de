---
title: Session. Timeout-Eigenschaft (WSManDisp. h)
description: Legt die maximale Zeitspanne (in Millisekunden) fest, die die Client Anwendung wartet, bis Windows-Remoteverwaltung den Vorgang beendet.
ms.assetid: ca35722a-1fd3-48bf-a11b-4624cb81aae3
ms.tgt_platform: multiple
keywords:
- Timeout-Eigenschaft Windows-Remoteverwaltung
- Timeout-Eigenschaft Windows-Remoteverwaltung, Session-Objekt
- Sitzungs Objekt Windows-Remoteverwaltung, Timeout-Eigenschaft
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
ms.openlocfilehash: c6c28b5284d9061e1c80fb3c66193d394c347a18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341358"
---
# <a name="sessiontimeout-property"></a>Session. Timeout (Eigenschaft)

Legt die maximale Zeitspanne (in Millisekunden) fest, die die Client Anwendung wartet, bis Windows-Remoteverwaltung den Vorgang beendet.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Session.Timeout As long
```



## <a name="property-value"></a>Eigenschaftswert

Timeout Wert in Millisekunden. Wenn der Timeout Wert überschritten wird, tritt ein Laufzeitfehler auf.

## <a name="remarks"></a>Bemerkungen

Der Timeout Wert kann vor jedem vom Agent ausgeführten Vorgang festgelegt werden. Wenn kein Timeout Wert angegeben wird, legt der Agent den Timeout Wert fest.

Während eines Enumerationsvorgangs kann der Timeout Wert nicht zurückgesetzt werden, während die Ressource aufgezählt wird.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird ein Calc.exe Prozess mit der [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) -Methode der WMI- [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Klasse gestartet. Der *strinputparameters* -Parameter enthält die Eingabeparameter im XML-Format. Das Skript gibt ein Timeout für die Sitzung an.


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
| Header<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sitzung**](session.md)
</dt> </dl>

 

