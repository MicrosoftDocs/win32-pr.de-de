---
title: Session. Create-Methode (WSManDisp. h)
description: Erstellt eine neue Instanz einer Ressource und gibt den Endpunkt Verweis (EPR) des neuen-Objekts zurück.
ms.assetid: 7629dfff-6c66-4b09-81a4-b1458ff977fa
ms.tgt_platform: multiple
keywords:
- Create-Methode Windows-Remoteverwaltung
- Create-Methode Windows-Remoteverwaltung, Session-Objekt
- Sitzungs Objekt Windows-Remoteverwaltung, Create-Methode
topic_type:
- apiref
api_name:
- Session.Create
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eacdbdffb9e2dac219e3922cabfc5615de34e69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477685"
---
# <a name="sessioncreate-method"></a>Session. Create-Methode

Erstellt eine neue Instanz einer Ressource und gibt den [*Endpunkt Verweis (EPR)*](windows-remote-management-glossary.md) des neuen-Objekts zurück.

## <a name="syntax"></a>Syntax


```VB
Session.Create( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*resourceUri* \[ in\]
</dt> <dd>

Der Bezeichner der zu erstellenden Ressource.

Dieser Parameter kann einen der folgenden Parameter enthalten:

-   Der URI mit mindestens einem [*Selektoren*](windows-remote-management-glossary.md). Beachten Sie, dass das [*WMI-Plug-in*](windows-remote-management-glossary.md) das Erstellen einer anderen Ressource als einem [WS-Management-Protokoll](ws-management-protocol.md) Listener nicht unterstützt.
-   [**ResourceLocator**](resourcelocator.md) -Objekt, das Selektoren, [*Fragmente*](windows-remote-management-glossary.md)oder [*Optionen*](windows-remote-management-glossary.md)enthalten kann.
-   Endpunkt Verweis der [*WS-Adressierung*](windows-remote-management-glossary.md) , wie im WS-Management Protocol-Standard beschrieben. Weitere Informationen zur öffentlichen Spezifikation WS-Management Protokolls finden Sie unter [Verwaltungs Spezifikationen Index page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*resource* 
</dt> <dd>

Der XML-Code, der Ressourcen Inhalt enthält.

</dd> <dt>

*Flags* \[ in, optional\]
</dt> <dd>

Reserviert. Muss auf 0 festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die EPR der neuen Ressource.

## <a name="remarks"></a>Bemerkungen

**Session. Create** wird nur zum Erstellen neuer Instanzen einer Ressource verwendet. Verwenden Sie die [**Session. Put**](session-put.md) -Methode, um vorhandene Instanzen einer Ressource zu aktualisieren. Nachdem Sie den neuen Ressourcen-URI erhalten haben, können Sie [**Session. Get**](session-get.md) aufrufen, um das neue-Objekt abzurufen. Das neue-Objekt enthält alle Eigenschaften, die der Ressourcenanbieter beim Erstellen des neuen-Objekts zuweist. Wenn Sie z. b. einen neuen [*WS-Management*](windows-remote-management-glossary.md) Protokolllistener erstellen und das Listenerobjekt mithilfe von **Session. Get** abrufen, erhalten Sie auch die Eigenschaften **Port**, **aktiviert** und **listeningon** .

Beachten Sie, dass das [*WMI-Plug-in*](windows-remote-management-glossary.md) keine Unterstützung für das Erstellen von Ressourcen bietet, die keine WS-Management Protokolllistener sind.

Die folgende Syntax wird verwendet, um diese Methode aufzurufen.


```VB
uri = session.Create("<resourceUri>", "<resource>")
```



## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird **Session. Create** aufgerufen, um einen Listener auf dem lokalen Computer zu erstellen.


```VB
'Create a WSMan object
Set oWsman = CreateObject( "WSMAN.Automation" )

'Create a Session object
Set oSession = oWsman.CreateSession

'Define resourceUri and inputXml 
resourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "config/Listener?Address=*+Transport=HTTP"

inputXml = _
    "<cfg:Listener xmlns:cfg=""https://schemas.dmtf.org/wbem/wsman/1/"_
    & "config/Listener.xsd"">" _
    & "<cfg:Hostname>" & GetFQDNName() & "</cfg:Hostname>" _            
    & "</cfg:Listener>"

'Perform the create operation.
response = oSession.Create( resourceUri, inputXml )
WScript.Echo "Response message: " & Chr(10) & response

Function GetFQDNName()
    Dim oShell, userDNSDomain, localComputerName
    Set oShell = CreateObject("WScript.Shell")
    userDNSDomain = oShell.ExpandEnvironmentStrings("%USERDNSDOMAIN%")

    localComputerName = _
        oShell.ExpandEnvironmentStrings("%ComputerName%")
    If userDNSDomain = "%USERDNSDOMAIN%" Then
        GetFQDNName= localComputerName
    Else
        GetFQDNName= localComputerName & "." & userDNSDomain
    End If
End Function
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
</dt> <dt>

[WS-Verwaltungsprotokoll](ws-management-protocol.md)
</dt> </dl>

 

