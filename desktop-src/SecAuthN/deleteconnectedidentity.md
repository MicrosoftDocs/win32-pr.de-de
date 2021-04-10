---
description: Löscht die Benutzer Anmelde Informationen, die für die verbundene Identität verwendet werden.
ms.assetid: EB32832D-9A8C-4CEB-897A-7E9D24FF84DD
title: Deleteconnectedidentity-Funktion (indentitystore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteConnectedIdentity
api_type:
- HeaderDef
api_location:
- Indentitystore.h
ms.openlocfilehash: 8079985f916e996a56b4203ad6ad065c1b7664e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041610"
---
# <a name="deleteconnectedidentity-function"></a>Deleteconnectedidentity-Funktion

Löscht die Benutzer Anmelde Informationen, die für die verbundene Identität verwendet werden.

## <a name="syntax"></a>Syntax


```C++
SEC_ENTRY DeleteConnectedIdentity(
  _In_     PVOID  ProviderHandle,
  _In_opt_ HANDLE UserToken,
  _In_     PSID   UserSid,
  _In_     PWSTR  IdentityUserName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProviderHandle* \[ in\]
</dt> <dd>

Handle des Identitäts Anbieters.

</dd> <dt>

*UserToken* \[ in, optional\]
</dt> <dd>

Token des verbundenen Benutzers, dessen Konto in ein lokales Konto konvertiert werden soll. Wenn *userToken* nicht **null** ist, verwendet der Identitäts Anbieter dieses Token, um das Benutzerprofil zu laden und verbundene Zustände zu bereinigen. Wenn *userToken* auf **null** festgelegt ist, erzwingt LSA die Trennung der Verbindung. Der Identitäts Anbieter sollte alle globalen verbundenen Zustände für diesen Benutzer bereinigen, aber der Anbieter muss keine verbundenen Zustände im Benutzerprofil bereinigen.

</dd> <dt>

*UserSID* \[ in\]
</dt> <dd>

Die primäre SID des verbundenen Benutzers. Wenn *userToken* nicht **null** ist, ist dieser Parameter die Benutzer-SID des Tokens. Wenn *userToken* **null** ist, wird dieser Parameter zum Identifizieren des verbundenen Benutzers und zum Bereinigen der Global verbundenen Zustände dieses Benutzers verwendet.

</dd> <dt>

*Identityusername* \[ in\]
</dt> <dd>

Der Benutzername der Identität.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion sec \_ E \_ OK zurück.

Wenn die Funktion fehlschlägt, gibt die Funktion möglicherweise einen der folgenden Fehlercodes zurück.



| Rückgabewert                                                                                               | BESCHREIBUNG                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>\_ungültiger \_ Parameter.</dt> </dl>      | Ein Parameter ist nicht gültig.<br/>                                                                                                                        |
| <dl> <dt>Status " \_ kein \_ solcher \_ Benutzer"</dt> </dl>          | Der von *UserSID* identifizierte Benutzer ist nicht vorhanden, ist zurzeit nicht verbunden, oder es ist keine Identität vorhanden, deren Benutzername mit *identityusername* übereinstimmt.<br/> |
| <dl> <dt>\_nicht genügend \_ Ressourcen.</dt> </dl> | Es ist nicht genügend Arbeitsspeicher vorhanden, um die Anforderung zu verarbeiten.<br/>                                                                                               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                  |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Indentitystore. h</dt> </dl> |



 

 




