---
title: ConnectionOptions. UserName-Eigenschaft (WSManDisp. h)
description: Hiermit wird der Benutzername eines lokalen Kontos oder eines Domänen Kontos auf dem Remote Computer festgelegt und abgerufen. Diese Eigenschaft bestimmt den Benutzernamen für die Authentifizierung.
ms.assetid: e8f70143-f002-4b39-97a3-006b9713262d
ms.tgt_platform: multiple
keywords:
- Username-Eigenschaft Windows-Remoteverwaltung
- Username-Eigenschaft Windows-Remoteverwaltung, ConnectionOptions-Objekt
- ConnectionOptions-Objekt Windows-Remoteverwaltung, UserName-Eigenschaft
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
ms.openlocfilehash: ba4d6c751dbe579372b863566412e740c2a646a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104583"
---
# <a name="connectionoptionsusername-property"></a>ConnectionOptions. Username (Eigenschaft)

Hiermit wird der Benutzername eines lokalen Kontos oder eines Domänen Kontos auf dem Remote Computer festgelegt und abgerufen. Diese Eigenschaft bestimmt den Benutzernamen für die Authentifizierung. Weitere Informationen finden Sie unter [Authentifizierung für Remote Verbindungen](authentication-for-remote-connections.md).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
ConnectionOptions.UserName As String
```



## <a name="property-value"></a>Eigenschaftswert

Eine Zeichenfolge, die den Benutzernamen eines lokalen Kontos oder eines Domänen Kontos auf dem Remote Computer enthält.

Wenn kein Wert angegeben ist und das **wsmanflagkredusernamepassword** -Flag nicht festgelegt ist, wird der Benutzername des Kontos verwendet, von dem das Skript ausgeführt wird.

Wenn kein Wert angegeben und das **wsmanflagdedusernamepassword** -Flag festgelegt ist, fordert das Skript den Benutzer zur Eingabe von Benutzername und Kennwort auf. Wenn kein gültiger Benutzername und kein gültiger Kennwort eingegeben werden, wird ein Fehler vom Typ "Zugriff verweigert" zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die folgende Syntax wird verwendet, um diese Eigenschaft anzugeben.


```VB
Set ConnectionOptions = wsman.CreateConnectionOptions
ConnectionOptions.UserName = "<UserName>"
```



Sie können **Benutzername** und [**Kennwort**](connectionoptions-password.md) für ein Domänen Konto angeben, wenn Sie eine [*Aushandlungs*](windows-remote-management-glossary.md) -oder *Kerberos* - [*Authentifizierung oder*](windows-remote-management-glossary.md) ein lokales Konto mit Standard Authentifizierung verwenden. Zum Herstellen einer Verbindung mit einem lokalen Konto müssen die [**WSMAN. kreatesession**](wsman-createsession.md) -Flags die Kombination aus dem **wsmanflagusebasic** -Flag und dem **wsmanflagkredusernamepassword** -Flag enthalten. Zum Herstellen einer Verbindung mit einem Domänen Konto müssen die **WSMAN. kreatesession** -Flags die Kombination aus dem **wsmanflagusenegotiate** -Flag und dem **wsmanflagkredusernamepassword** -Flag oder die Kombination aus dem **wsmanflagusekerberos** -Flag und dem **wsmanflagkredusernamepassword** -Flag enthalten. Für ein Domänen Konto muss der **Benutzername** im Format "Computer \\ Benutzername" angegeben werden, wobei der "Computer"-Teil der Zeichenfolge entweder der Name oder die IP-Adresse sein kann. Weitere Informationen finden Sie unter [Authentifizierung für Remote Verbindungen](authentication-for-remote-connections.md).


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseBasic Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



Zum Herstellen einer Verbindung mit einem Domänen Konto müssen die [**WSMAN. kreatesession**](wsman-createsession.md) -Flags die Kombination aus dem **wsmanflagusenegotiate** -Flag und dem **wsmanflagkredusernamepassword** -Flag für das Herstellen einer Verbindung mit einem Domänen Konto enthalten, das eine Aushandlungs Authentifizierung erfordert.


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
| Header<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> </dl>

 

 





