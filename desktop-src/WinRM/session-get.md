---
title: Session.Get-Methode (WSManDisp.h)
description: Ruft die durch den URI angegebene Ressource ab und gibt eine XML-Darstellung der aktuellen Instanz der Ressource zurück.
ms.assetid: 873242fd-9da3-42f4-a18e-258fedba77ec
ms.tgt_platform: multiple
keywords:
- Abrufen der Methode Windows Remoteverwaltung
- Abrufen der Methode Windows Remoteverwaltung, Sitzungsobjekt
- Sitzungsobjekt Windows Remoteverwaltung , Get-Methode
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
ms.openlocfilehash: 9c983c5f95ddfa3acc88b85b383ec85ddf85f885293031fe9bc4e4e07c90850a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642560"
---
# <a name="sessionget-method"></a>Session.Get-Methode

Ruft die durch den [*URI*](windows-remote-management-glossary.md) angegebene Ressource ab und gibt eine XML-Darstellung der aktuellen Instanz der Ressource zurück.

## <a name="syntax"></a>Syntax


```VB
Session.Get( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*resourceUri* \[ In\]
</dt> <dd>

Der Bezeichner der abzurufenden Ressource.

Dieser Parameter kann eine der folgenden Elemente enthalten:

-   Ein URI mit oder ohne [*Selektoren.*](windows-remote-management-glossary.md) Wenn Sie die **Get-Methode** mit einem Selektor aufrufen, um eine WMI-Ressource abzurufen, verwenden Sie die Schlüsseleigenschaft oder die Eigenschaften des Objekts. Im folgenden Codebeispiel Visual Basic Scripting Edition (VBScript) wird der Schlüssel beispielsweise durch `Win32_Service?Name=winmgmt` angegeben. Für Singletonklassen wie [**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime)können Sie keinen Selektor verwenden.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_LocalTime"
    ```

    

-   Ein [**ResourceLocator-Objekt,**](resourcelocator.md) das [*Selektoren, Fragmente*](windows-remote-management-glossary.md)oder [*Optionen*](windows-remote-management-glossary.md)enthalten kann.
-   Ein [*WS-Adressierungsendpunktverweis,*](windows-remote-management-glossary.md) wie im WS-Management-Protokollstandard beschrieben. Weitere Informationen zur öffentlichen Spezifikation für WS-Management-Protokoll finden [Sie](ws-management-protocol.md)unter Indexseite der [Verwaltungsspezifikationen.](/previous-versions/dotnet/articles/ms951267(v=msdn.10))

</dd> <dt>

*Flags* \[ in, optional\]
</dt> <dd>

Reserviert. Muss auf 0 festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine XML-Darstellung der Ressource.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird die XML-Darstellung der [**\_ Win32-Dienstinstanz**](/windows/desktop/CIMWin32Prov/win32-service) abgerufen, die den WMI-Winmgmt-Dienst auf dem lokalen Computer darstellt.


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



Im folgenden VBScript-Codebeispiel wird die WMI Winmgmt-Dienstinstanz von einem Remotecomputer abgerufen. Der Remotecomputer wird durch den vollqualifizierten Domänennamen (servername.domain.com) identifiziert. Der einzige Unterschied zwischen der lokalen Version und der Remoteversion ist die Spezifikation des Remotecomputers im Aufruf von [**WSMan.CreateSession.**](wsman-createsession.md)


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
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sitzung**](session.md)
</dt> </dl>

 

