---
title: Session. aufrufen-Methode (WSManDisp. h)
description: Ruft eine Methode auf und gibt die Ergebnisse des Methodenaufrufs zurück.
ms.assetid: c83d0631-2efb-47d9-abcf-ab0c8de06c36
ms.tgt_platform: multiple
keywords:
- Methoden Windows-Remoteverwaltung aufrufen
- Methoden Windows-Remoteverwaltung aufrufen, Sitzungs Objekt
- Sitzungs Objekt Windows-Remoteverwaltung, Methode "aufrufen"
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
ms.openlocfilehash: 117c688b616f377730524a09234b1dc38a4996c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743224"
---
# <a name="sessioninvoke-method"></a>Session. aufrufen-Methode

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

*Aktions-URI* \[ in\]
</dt> <dd>

Der URI der aufzurufenden Methode.

</dd> <dt>

*resourceUri* \[ in\]
</dt> <dd>

Der Bezeichner der abzurufenden Ressource.

Dieser Parameter kann einen der folgenden Parameter enthalten:

-   URI mit oder ohne [*Selektoren*](windows-remote-management-glossary.md). Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird der Schlüssel durch angegeben `Win32_Service?Name=winmgmt` .

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _ 
       & "Win32_Service?Name=winmgmt"
    ```

    

-   [**ResourceLocator**](resourcelocator.md) -Objekt, das Selektoren, [*Fragmente*](windows-remote-management-glossary.md)oder [*Optionen*](windows-remote-management-glossary.md)enthalten kann.
-   Endpunkt Verweis der [*WS-Adressierung*](windows-remote-management-glossary.md) , wie im [WS-Management-Protokoll](ws-management-protocol.md) -Standard beschrieben. Weitere Informationen zur öffentlichen Spezifikation WS-Management Protokolls finden Sie unter [Verwaltungs Spezifikationen Index page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*Parameter* \[ in\]
</dt> <dd>

Die XML-Darstellung der Eingabe für die Methode. Diese Zeichenfolge muss angegeben werden, oder diese Methode schlägt fehl.

</dd> <dt>

*Flags* \[ in, optional\]
</dt> <dd>

Reserviert. Muss auf 0 festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die XML-Darstellung der Methoden Ausgabe.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird ein Calc.exe Prozess gestartet. Der *strinputparameters* -Parameter enthält die Eingabeparameter im XML-Format. Der einzige erforderliche Eingabeparameter für die [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) -Methode der WMI- [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Klasse ist die auszuführende Befehlszeile.


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



Im folgenden VBScript-Codebeispiel wird die **Session. aufrufen** -Methode aufgerufen, um die [**Stop Service**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service) -Methode des [**Win32- \_ Dienstanbieter**](/windows/desktop/CIMWin32Prov/win32-service)auszuführen. Die **Stop Service** -Methode hat keine Eingabeparameter. Die **Aufruf** Methode erfordert jedoch eine XML-Zeichenfolge im *Parameter para* meters.


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
| Header<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sitzung**](session.md)
</dt> </dl>

 

