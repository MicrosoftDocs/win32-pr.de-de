---
title: ConnectionOptions-Objekt (WSManDisp.h)
description: Das ConnectionOptions-Objekt wird an die CreateSession-Methode übergeben, um den Benutzernamen und das Kennwort für das lokale Konto auf dem Remotecomputer einzugeben.
ms.assetid: 7a87a5f7-78ed-452c-9b9f-ad48811a3339
ms.tgt_platform: multiple
keywords:
- ConnectionOptions-Objekt Windows Remoteverwaltung
- ConnectionOptions-Objekt Windows Remoteverwaltung , beschrieben
topic_type:
- apiref
api_name:
- ConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8665dc3a5be91fddb4332be3512ec9eec5c483495a21b95b641ec26e4e9e111
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734090"
---
# <a name="connectionoptions-object"></a>ConnectionOptions-Objekt

Das **ConnectionOptions-Objekt** wird an die [**CreateSession-Methode**](wsman-createsession.md) übergeben, um den Benutzernamen und das Kennwort für das lokale Konto auf dem Remotecomputer einzugeben. Wenn keine Parameter angegeben werden, werden die Anmeldeinformationen des Kontos, das das Skript ausgeführt, auf die Standardwerte festgelegt.

## <a name="members"></a>Member

Das **ConnectionOptions-Objekt** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **ConnectionOptions-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                  | Zugriffstyp           | Beschreibung                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [**Kennwort**](connectionoptions-password.md)<br/> | Lesegeschützt<br/> | Legt das Kennwort eines lokalen Kontos oder Domänenkontos auf dem Remotecomputer fest.<br/>           |
| [**Nutzername**](connectionoptions-username.md)<br/> | Lesen/Schreiben<br/> | Legt den Benutzernamen eines lokalen Kontos oder eines Domänenkontos auf dem Remotecomputer fest und ruft den Benutzernamen ab.<br/> |



 

## <a name="remarks"></a>Hinweise

Das **ConnectionOptions-Objekt** entspricht der [**IWSManConnectionOptions-Schnittstelle.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)

Wenn eine Windows Remoteverwaltungsclientanwendung unter Identitätswechsel ausgeführt wird, tritt ein Fehler auf, wenn Sie die [**Password-Eigenschaft**](connectionoptions-password.md) festlegen. Eine Clientanwendung ist ein Skript oder ein anderes Programm, das eine Anforderung an WinRM auf dem lokalen oder einem Remotecomputer sendet. Die Clientanwendung wird möglicherweise unter Identitätswechsel ausgeführt, da sie eine Funktion wie [**ImpersonateClient aufgerufen hat.**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)) Eine Active Server-Seite (ASP) oder ein Dienst kann keinen Benutzernamen und kein Kennwort anfordern, wenn der ASP-Prozess unter einem Konto ausgeführt wird, das die Identität eines Clients anfing.

Das **WSManFlagCredUserNamePassword-Flag** sollte für den [**WSman.CreateSession-Aufruf**](wsman-createsession.md) festgelegt werden, wenn [**UserName**](connectionoptions-username.md) und Password für die Authentifizierung [**verwendet**](connectionoptions-password.md) werden.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie Sie ein **ConnectionOptions-Objekt** erstellen, die Eigenschaften für das Konto auf dem Remotecomputer festlegen und es zum Erstellen eines [**Session-Objekts verwenden.**](session.md)


```VB
Set objWsman = CreateObject( "Wsman.Automation" )
'Create ConnectionOptions object.
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "johns "
objConnectionOptions.Password = "Dtf#4542?98"
iFlags = objWsman.SessionFlagUseBasic Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession _
  ("https://172.30.168.2", iFlags, objConnectionOptions)
strResource = objSession.Get("winrm/config")
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

[Authentifizierung für Remoteverbindungen](authentication-for-remote-connections.md)
</dt> <dt>

[WinRM-Skripterstellungs-API](winrm-scripting-api.md)
</dt> <dt>

[Informationen Windows Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Verwenden Windows Remoteverwaltung](using-windows-remote-management.md)
</dt> <dt>

[Skripterstellung in Windows Remoteverwaltung](scripting-in-windows-remote-management.md)
</dt> <dt>

[Abrufen von Daten vom lokalen Computer](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Abrufen von Daten von einem Remotecomputer](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

