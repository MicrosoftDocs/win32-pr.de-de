---
description: Löscht die Benutzer-Anmeldeinformationen, die für die verbundene Identität verwendet werden.
ms.assetid: EB32832D-9A8C-4CEB-897A-7E9D24FF84DD
title: DeleteConnectedIdentity-Funktion (Indentitystore.h)
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
ms.openlocfilehash: 7e59beeb17f7d6d0cced96daaceef7440523c3ce603d759f18cc69a93c0ab05c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008468"
---
# <a name="deleteconnectedidentity-function"></a>DeleteConnectedIdentity-Funktion

Löscht die Benutzer-Anmeldeinformationen, die für die verbundene Identität verwendet werden.

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

*ProviderHandle* \[ In\]
</dt> <dd>

Identitätsanbieterhand handle.

</dd> <dt>

*UserToken* \[ in, optional\]
</dt> <dd>

Token des verbundenen Benutzers, dessen Konto in ein lokales Konto konvertiert werden soll. Wenn *UserToken* nicht **NULL ist,** verwendet der Identitätsanbieter dieses Token, um das Benutzerprofil zu laden und verbundene Zustände zu bereinign. Wenn *UserToken* NULL **ist,** erzwingt LSA die Trennung. Der Identitätsanbieter sollte alle globalen verbundenen Zustände für diesen Benutzer bereinigt, der Anbieter muss jedoch keine verbundenen Zustände im Benutzerprofil bereinigt.

</dd> <dt>

*UserSid* \[ In\]
</dt> <dd>

Die primäre SID des verbundenen Benutzers. Wenn *UserToken* nicht **NULL ist,** ist dieser Parameter die Benutzer-SID des Tokens. Wenn *UserToken* **NULL ist,** wird dieser Parameter verwendet, um den verbundenen Benutzer zu identifizieren und globale verbundene Zustände dieses Benutzers zu bereinign.

</dd> <dt>

*IdentityUserName* \[ In\]
</dt> <dd>

Der Benutzername der Identität.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt die Funktion SEC \_ E \_ OK zurück.

Wenn die Funktion fehlschlägt, gibt die Funktion möglicherweise einen der folgenden Fehlercodes zurück.



| Rückgabewert                                                                                               | BESCHREIBUNG                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>STATUS \_ UNGÜLTIGER \_ PARAMETER</dt> </dl>      | Ein Parameter ist nicht gültig.<br/>                                                                                                                        |
| <dl> <dt>STATUS \_ KEIN \_ SOLCHER \_ BENUTZER</dt> </dl>          | Der von *UserSid identifizierte* Benutzer ist nicht vorhanden, ist derzeit nicht verbunden, oder es ist keine Identität vorhanden, deren Benutzername *IdentityUserName entspricht.*<br/> |
| <dl> <dt>STATUS \_ UNZUREICHENDE \_ RESSOURCEN</dt> </dl> | Es ist nicht genügend Arbeitsspeicher vorhanden, um die Anforderung zu verarbeiten.<br/>                                                                                               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Indentitystore.h</dt> </dl> |



 

 




