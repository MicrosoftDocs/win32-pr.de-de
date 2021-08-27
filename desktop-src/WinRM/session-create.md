---
title: Session.Create-Methode (WSManDisp.h)
description: Erstellt eine neue Instanz einer Ressource und gibt den Endpunktverweis (Endpoint Reference, EPR) des neuen -Objekts zurück.
ms.assetid: 7629dfff-6c66-4b09-81a4-b1458ff977fa
ms.tgt_platform: multiple
keywords:
- Erstellen einer Windows Remoteverwaltung
- Erstellen einer Methode Windows Remoteverwaltung, Sitzungsobjekt
- Sitzungsobjekt Windows Remoteverwaltung , Create-Methode
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
ms.openlocfilehash: 97adac133adc4c636de395f564927a5f0194b3c52d50685ac034142e6c15aadf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823262"
---
# <a name="sessioncreate-method"></a>Session.Create-Methode

Erstellt eine neue Instanz einer Ressource und gibt den [*Endpunktverweis (Endpoint Reference, EPR)*](windows-remote-management-glossary.md) des neuen -Objekts zurück.

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

*resourceUri* \[ In\]
</dt> <dd>

Bezeichner der zu erstellenden Ressource.

Dieser Parameter kann eine der folgenden Elemente enthalten:

-   URI mit mindestens einem [*Selektor.*](windows-remote-management-glossary.md) Beachten Sie, dass [*das WMI-Plug-In*](windows-remote-management-glossary.md) das Erstellen einer anderen Ressource als eines WS-Management-Protokoll [unterstützt.](ws-management-protocol.md)
-   [**ResourceLocator-Objekt,**](resourcelocator.md) das Selektoren, [*Fragmente oder*](windows-remote-management-glossary.md)Optionen enthalten [*kann.*](windows-remote-management-glossary.md)
-   [*WS-Adressierungsendpunktreferenz,*](windows-remote-management-glossary.md) wie im WS-Management-Protokollstandard beschrieben. Weitere Informationen zur öffentlichen Spezifikation für das WS-Management finden Sie auf der [Indexseite für Verwaltungsspezifikationen.](/previous-versions/dotnet/articles/ms951267(v=msdn.10))

</dd> <dt>

*resource* 
</dt> <dd>

Der XML-Code, der Ressourceninhalt enthält.

</dd> <dt>

*Flags* \[ in, optional\]
</dt> <dd>

Reserviert. Muss auf 0 festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der EPR der neuen Ressource.

## <a name="remarks"></a>Hinweise

**Session.Create** wird nur zum Erstellen neuer Instanzen einer Ressource verwendet. Verwenden Sie [**die Session.Put-Methode,**](session-put.md) um vorhandene Instanzen einer Ressource zu aktualisieren. Nachdem Sie den neuen Ressourcen-URI abgerufen haben, können Sie [**Session.Get aufrufen,**](session-get.md) um das neue Objekt abzurufen. Das neue -Objekt enthält alle Eigenschaften, die der Ressourcenanbieter beim Erstellen des neuen Objekts zuweist. Wenn Sie beispielsweise einen neuen WS-Management-Protokolllistener erstellen und das Listenerobjekt mit **Session.Get** abrufen, rufen Sie auch die **Eigenschaften Port**, **Enabled** und [](windows-remote-management-glossary.md) **ListeningOn** ab.

Beachten Sie, dass [*das WMI-Plug-In*](windows-remote-management-glossary.md) das Erstellen einer anderen Ressource als eines WS-Management unterstützt.

Die folgende Syntax wird zum Aufrufen dieser Methode verwendet.


```VB
uri = session.Create("<resourceUri>", "<resource>")
```



## <a name="examples"></a>Beispiele

Das folgende VBScript-Codebeispiel ruft **Session.Create auf,** um einen Listener auf dem lokalen Computer zu erstellen.


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
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Sitzungskonsistenz**](session.md)
</dt> <dt>

[WS-Verwaltungsprotokoll](ws-management-protocol.md)
</dt> </dl>

 

