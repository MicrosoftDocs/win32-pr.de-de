---
title: Session.Invoke-Methode (WSManDisp.h)
description: Ruft eine Methode auf und gibt die Ergebnisse des Methodenaufrufs zurück.
ms.assetid: c83d0631-2efb-47d9-abcf-ab0c8de06c36
ms.tgt_platform: multiple
keywords:
- Aufrufen der Methode Windows Remoteverwaltung
- Aufrufen der Methode Windows Remoteverwaltung, Sitzungsobjekt
- Sitzungsobjekt Windows Remoteverwaltung, Invoke-Methode
topic_type:
- apiref
api_name:
- Session.Invoke
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2afa20390890c53a7362d776c1df7c84d0a638e7fcb10269c901d194a50dea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743251"
---
# <a name="sessioninvoke-method"></a>Session.Invoke-Methode

Ruft eine Methode auf und gibt die Ergebnisse des Methodenaufrufs zurück.

## <a name="syntax"></a>Syntax


```VB
Session.Invoke( _
  ByVal actionUri, _
  ByVal resourceUri, _
  ByVal parameters, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*actionUri* \[ In\]
</dt> <dd>

Der URI der aufzurufende Methode.

</dd> <dt>

*resourceUri* \[ In\]
</dt> <dd>

Der Bezeichner der abzurufenden Ressource.

Dieser Parameter kann eine der folgenden Elemente enthalten:

-   URI mit oder ohne [*Selektoren.*](windows-remote-management-glossary.md) Im folgenden Beispiel Visual Basic Scripting Edition (VBScript) wird der Schlüssel durch `Win32_Service?Name=winmgmt` angegeben.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _ 
       & "Win32_Service?Name=winmgmt"
    ```

    

-   [**ResourceLocator-Objekt,**](resourcelocator.md) das [*Selektoren, Fragmente*](windows-remote-management-glossary.md)oder [*Optionen*](windows-remote-management-glossary.md)enthalten kann.
-   [*WS-Adressierungsendpunktverweis,*](windows-remote-management-glossary.md) wie im [WS-Management-Protokoll](ws-management-protocol.md) Standard beschrieben. Weitere Informationen zur öffentlichen Spezifikation für WS-Management-Protokoll finden Sie auf der Indexseite der [Verwaltungsspezifikationen.](/previous-versions/dotnet/articles/ms951267(v=msdn.10))

</dd> <dt>

*Parameter* \[ In\]
</dt> <dd>

Die XML-Darstellung der Eingabe für die Methode. Diese Zeichenfolge muss angegeben werden, andernfalls schlägt diese Methode fehl.

</dd> <dt>

*Flags* \[ in, optional\]
</dt> <dd>

Reserviert. Muss auf 0 festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die XML-Darstellung der Methodenausgabe.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird ein Calc.exe Prozess gestartet. Der *parameter strInputParameters* enthält die Eingabeparameter im XML-Format. Der einzige erforderliche Eingabeparameter für die [**Create-Methode**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) der WMI [**Win32 \_ Process-Klasse**](/windows/desktop/CIMWin32Prov/win32-process) ist die auszuführende Befehlszeile.


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



Im folgenden VBScript-Codebeispiel wird die **Session.Invoke-Methode** aufgerufen, um die [**StopService-Methode**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service) des [**Win32-Diensts \_**](/windows/desktop/CIMWin32Prov/win32-service)auszuführen. Die **StopService-Methode** verfügt nicht über Eingabeparameter. Die **Invoke-Methode** erfordert jedoch eine XML-Zeichenfolge im *parameter-Parameter.*


```VB
Option Explicit

Dim objWsman
Dim objSession
Dim strResponse
Dim strActionURI
Dim strInputXml
Dim strResourceURI
Dim strMethodName

set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession
strResourceURI = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=w32time"
strMethodName = "StopService"
strActionURI = strMethodName                                      

strInputXml = "<p:StopService_INPUT " _
    & "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service""/>"

strResponse = objSession.Invoke(strMethodName, strResourceURI, strInputXml)

call DisplayOutput(strResponse)
 
strMethodName = "StartService" 
strActionURI = strResourceURI & "/" & strMethodName  
strInputXml = "<p:StartService_INPUT " _
    & "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service""/>"
strResponse = objSession.Invoke(strMethodName, _
    strResourceURI, strInputXml)

call DisplayOutput(strResponse)

 
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

 

