---
title: ConnectionOptions-Objekt (WSManDisp. h)
description: Das ConnectionOptions-Objekt wird an die Methode "kreatesession" übergeben, um den Benutzernamen und das Kennwort anzugeben, die dem lokalen Konto auf dem Remote Computer zugeordnet sind.
ms.assetid: 7a87a5f7-78ed-452c-9b9f-ad48811a3339
ms.tgt_platform: multiple
keywords:
- ConnectionOptions-Objekt Windows-Remoteverwaltung
- ConnectionOptions-Objekt Windows-Remoteverwaltung, beschrieben
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
ms.openlocfilehash: 164eb886ce98266cab3109e773b731e002d1abac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343454"
---
# <a name="connectionoptions-object"></a>ConnectionOptions-Objekt

Das **ConnectionOptions** -Objekt wird an die Methode " [**kreatesession**](wsman-createsession.md) " übergeben, um den Benutzernamen und das Kennwort anzugeben, die dem lokalen Konto auf dem Remote Computer zugeordnet sind. Wenn keine Parameter angegeben werden, werden die Anmelde Informationen des Kontos, auf dem das Skript ausgeführt wird, auf die Standardwerte festgelegt.

## <a name="members"></a>Member

Das **ConnectionOptions** -Objekt verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **ConnectionOptions** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                  | Zugriffstyp           | BESCHREIBUNG                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [**Kennwort**](connectionoptions-password.md)<br/> | Lesegeschützt<br/> | Legt das Kennwort eines lokalen Kontos oder eines Domänen Kontos auf dem Remote Computer fest.<br/>           |
| [**User**](connectionoptions-username.md)<br/> | Lesen/Schreiben<br/> | Hiermit wird der Benutzername eines lokalen Kontos oder eines Domänen Kontos auf dem Remote Computer festgelegt und abgerufen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das **ConnectionOptions** -Objekt entspricht der [**iwsmanconnectionoptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) -Schnittstelle.

Wenn eine Windows-Remoteverwaltung Client Anwendung unter dem Identitätswechsel ausgeführt wird, tritt ein Fehler auf, wenn Sie die Kenn [**Wort**](connectionoptions-password.md) Eigenschaft festlegen. Bei einer Client Anwendung handelt es sich um ein Skript oder ein anderes Programm, das eine Anforderung an WinRM auf dem lokalen Computer oder auf einem Remote Computer sendet. Die Client Anwendung wird möglicherweise unter dem Identitätswechsel ausgeführt, da Sie eine [**Funktion wie "**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85))Identitätsnachweis Nachweis" genannt hat. Eine Active Server Seite (ASP) oder ein Dienst kann keinen Benutzernamen und kein Kennwort anfordern, wenn der ASP-Prozess unter einem Konto ausgeführt wird, das die Identität eines Clients annimmt.

Das Flag " **wsmanflagkredusernamepassword** " sollte für den [**WSMAN. anatesession**](wsman-createsession.md) -Befehl festgelegt werden, wenn der [**Benutzername**](connectionoptions-username.md) und das [**Kennwort**](connectionoptions-password.md) für die Authentifizierung verwendet werden.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie ein **ConnectionOptions** -Objekt erstellt, die Eigenschaften für das Konto auf dem Remote Computer festgelegt und beim Erstellen eines [**Sitzungs**](session.md) Objekts verwendet wird.


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
| Header<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Authentifizierung für Remote Verbindungen](authentication-for-remote-connections.md)
</dt> <dt>

[WinRM-Skript-API](winrm-scripting-api.md)
</dt> <dt>

[Informationen zu Windows-Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Verwenden von Windows-Remoteverwaltung](using-windows-remote-management.md)
</dt> <dt>

[Skripterstellung in Windows-Remoteverwaltung](scripting-in-windows-remote-management.md)
</dt> <dt>

[Abrufen von Daten vom lokalen Computer](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Abrufen von Daten von einem Remote Computer](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

