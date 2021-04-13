---
title: Session. Get-Methode (WSManDisp. h)
description: Ruft die vom URI angegebene Ressource ab und gibt eine XML-Darstellung der aktuellen Instanz der Ressource zurück.
ms.assetid: 873242fd-9da3-42f4-a18e-258fedba77ec
ms.tgt_platform: multiple
keywords:
- Get-Methode Windows-Remoteverwaltung
- Get-Methode Windows-Remoteverwaltung, Session-Objekt
- Sitzungs Objekt Windows-Remoteverwaltung, Get-Methode
topic_type:
- apiref
api_name:
- Session.Get
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e4ee84cc711db312389151d1dd95fb890474dcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341018"
---
# <a name="sessionget-method"></a>Session. Get-Methode

Ruft die vom [*URI*](windows-remote-management-glossary.md) angegebene Ressource ab und gibt eine XML-Darstellung der aktuellen Instanz der Ressource zurück.

## <a name="syntax"></a>Syntax


```VB
Session.Get( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*resourceUri* \[ in\]
</dt> <dd>

Der Bezeichner der abzurufenden Ressource.

Dieser Parameter kann einen der folgenden Parameter enthalten:

-   Ein URI mit oder ohne [*Selektoren*](windows-remote-management-glossary.md). Wenn Sie die **Get** -Methode mit einem Selektor aufrufen, um eine WMI-Ressource abzurufen, verwenden Sie die Schlüsseleigenschaft oder die Eigenschaften des Objekts. Beispielsweise wird im folgenden Visual Basic Scripting Edition Codebeispiel (VBScript) der Schlüssel durch angegeben `Win32_Service?Name=winmgmt` . Bei Singleton-Klassen, wie z. b. [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime), kann kein Selektor verwendet werden.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_LocalTime"
    ```

    

-   Ein [**ResourceLocator**](resourcelocator.md) -Objekt, das Selektoren, [*Fragmente*](windows-remote-management-glossary.md)oder [*Optionen*](windows-remote-management-glossary.md)enthalten kann.
-   Ein [*WS-adressierungsend*](windows-remote-management-glossary.md) Punkt Verweis, wie im WS-Management Protocol-Standard beschrieben. Weitere Informationen zur öffentlichen Spezifikation für [WS-Management-Protokoll](ws-management-protocol.md)finden Sie auf der [Seite Verwaltungs Spezifikationen Index](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*Flags* \[ in, optional\]
</dt> <dd>

Reserviert. Muss auf 0 festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine XML-Darstellung der Ressource.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird die XML-Darstellung der [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) Instanz abgerufen, die den WMI-WinMgmt-Dienst auf dem lokalen Computer darstellt.


```VB

'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 


strResourceUri = "http://schemas.microsoft.com/" _ 
    & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
If Err.Number <> 0 Then
    DisplayErrorInfo
End If
On Error Goto 0

Sub DisplayErrorInfo()
    WScript.Echo "An error has occurred."     
    WScript.Echo
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    WScript.Echo Err.Clear    
End Sub

```



Im folgenden VBScript-Codebeispiel wird die WMI-WinMgmt-Dienst Instanz von einem Remote Computer abgerufen. Der Remote Computer wird durch den voll qualifizierten Domänen Namen (Servername.Domain.com) identifiziert. Der einzige Unterschied zwischen der lokalen Version und der Remote Version ist die Angabe des Remote Computers im [**WSMAN. kreatesession**](wsman-createsession.md)-aufrufen.


```VB
Const RemoteComputer = "servername.domain.com"

'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Dim objSession
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 


strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/" _ 
    & "Win32_Service?Name=winmgmt"


On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
If Err.Number <> 0 Then
    DisplayErrorInfo
End If
On Error Goto 0

Sub DisplayErrorInfo()
    WScript.Echo "An error has occurred."     
    WScript.Echo
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    WScript.Echo Err.Clear    
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

 

