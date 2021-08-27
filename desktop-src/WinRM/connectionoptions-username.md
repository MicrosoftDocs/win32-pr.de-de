---
title: ConnectionOptions.UserName-Eigenschaft (WSManDisp.h)
description: Legt den Benutzernamen eines lokalen kontos oder eines Domänenkontos auf dem Remotecomputer fest und ruft den Benutzernamen ab. Diese Eigenschaft bestimmt den Benutzernamen für die Authentifizierung.
ms.assetid: e8f70143-f002-4b39-97a3-006b9713262d
ms.tgt_platform: multiple
keywords:
- UserName-Eigenschaft Windows Remoteverwaltung
- UserName-Eigenschaft Windows Remoteverwaltung, ConnectionOptions-Objekt
- ConnectionOptions-Objekt Windows Remoteverwaltung , UserName-Eigenschaft
topic_type:
- apiref
api_name:
- ConnectionOptions.UserName
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40fa4cd5e1d4fd733431adab80241744c0b197960506cfe2908bc99315ecfdea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121780"
---
# <a name="connectionoptionsusername-property"></a>ConnectionOptions.UserName-Eigenschaft

Legt den Benutzernamen eines lokalen kontos oder eines Domänenkontos auf dem Remotecomputer fest und ruft den Benutzernamen ab. Diese Eigenschaft bestimmt den Benutzernamen für die Authentifizierung. Weitere Informationen finden Sie unter [Authentifizierung für Remoteverbindungen.](authentication-for-remote-connections.md)

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
ConnectionOptions.UserName As String
```



## <a name="property-value"></a>Eigenschaftswert

Zeichenfolge, die den Benutzernamen eines lokalen kontos oder eines Domänenkontos auf dem Remotecomputer enthält.

Wenn kein Wert angegeben wird und das **Flag WSManFlagCredUsernamePassword** nicht festgelegt ist, wird der Benutzername des Kontos verwendet, das das Skript ausführt.

Wenn kein Wert angegeben und das **Flag WSManFlagCredUsernamePassword** festgelegt ist, fordert das Skript den Benutzer auf, den Benutzernamen und das Kennwort einzugeben. Wenn kein gültiger Benutzername und kein Kennwort eingegeben werden, wird ein Zugriffsverweigerungsfehler zurückgegeben.

## <a name="remarks"></a>Hinweise

Die folgende Syntax wird verwendet, um diese Eigenschaft anzugeben.


```VB
Set ConnectionOptions = wsman.CreateConnectionOptions
ConnectionOptions.UserName = "<UserName>"
```



Sie können **Benutzername** und [**Kennwort**](connectionoptions-password.md) für ein Domänenkonto bereitstellen, wenn Sie [*die Aushandlung*](windows-remote-management-glossary.md) oder *Kerberos-Authentifizierung* verwenden, oder für ein lokales Konto mit [*Standardauthentifizierung.*](windows-remote-management-glossary.md) Um eine Verbindung mit einem lokalen Konto herzustellen, müssen die [**WSMan.CreateSession-Flags**](wsman-createsession.md) die Kombination aus dem **WSManFlagUseBasic-Flag** und dem **WsmanFlagCredUserNamePassword-Flag** enthalten. Um eine Verbindung mit einem Domänenkonto herzustellen, müssen die **WSMan.CreateSession-Flags** die Kombination aus dem **Flag WSManFlagUseNegotiate** und dem **Flag WsmanFlagCredUserNamePassword** oder die Kombination aus dem **WSManFlagUseKerberos-Flag** und dem **WsmanFlagCredUserNamePassword-Flag** enthalten. Für ein Domänenkonto muss **UserName** im Format \\ "Computerbenutzername" angegeben werden, wobei der Teil "computer" der Zeichenfolge entweder der Name oder die IP-Adresse sein kann. Weitere Informationen finden Sie unter [Authentifizierung für Remoteverbindungen.](authentication-for-remote-connections.md)


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseBasic Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



Zum Herstellen einer Verbindung mit einem Domänenkonto müssen die [**WSMan.CreateSession-Flags**](wsman-createsession.md) die Kombination aus dem **Flag WSManFlagUseNegotiate** und dem **Flag WsmanFlagCredUserNamePassword** enthalten, um eine Verbindung mit einem Domänenkonto herzustellen, was eine Negotiate-Authentifizierung erfordert.


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseNegotiate Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
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

[**Connectionoptions**](connectionoptions.md)
</dt> </dl>

 

 





