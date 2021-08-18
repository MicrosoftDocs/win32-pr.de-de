---
description: Die AutohzGetCentralAccessPolicyCallback-Funktion ist eine anwendungsdefinierte Funktion, die die zentrale Zugriffsrichtlinie abruft. AuthzGetCentralAccessPolicyCallback ist ein Platzhalter für den anwendungsdefinierte Funktionsnamen.
ms.assetid: 1D5831EF-ACA8-4EE9-A7C1-E1A3CB74CEC0
title: AutohzGetCentralAccessPolicyCallback-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzGetCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5e8fd0afbd901d48386859e9b5d3557a173cfe6a23d749dc776992a4aedebed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783744"
---
# <a name="authzgetcentralaccesspolicycallback-callback-function"></a>AutohzGetCentralAccessPolicyCallback-Rückruffunktion

Die *AutohzGetCentralAccessPolicyCallback-Funktion* ist eine anwendungsdefinierte Funktion, die die zentrale Zugriffsrichtlinie abruft. *AuthzGetCentralAccessPolicyCallback* ist ein Platzhalter für den anwendungsdefinierte Funktionsnamen.

## <a name="syntax"></a>Syntax


```C++
BOOL CALLBACK AuthzGetCentralAccessPolicyCallback (
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PSID                        capid,
  _In_opt_ PVOID                       pArgs,
  _Out_    PBOOL                       pCentralAccessPolicyApplicable,
  _Out_    PVOID                       ppCentralAccessPolicy
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hAuthzClientContext* \[ In\]
</dt> <dd>

Handle für den Clientkontext.

</dd> <dt>

*capid* \[ In\]
</dt> <dd>

ID der abzurufende zentralen Zugriffsrichtlinie.

</dd> <dt>

*pArgs* \[ in, optional\]
</dt> <dd>

Optionale Argumente, die über den **OptionalArguments-Member** der AUTHZ ACCESS REQUEST-Struktur an die [**\_ AutohzAccessCheck-Funktion \_**](/windows/desktop/api/Authz/ns-authz-authz_access_request) übergeben wurden. [](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)

</dd> <dt>

*pCentralAccessPolicyApplicable* \[ out\]
</dt> <dd>

Zeiger auf einen booleschen Wert, den der Ressourcen-Manager verwendet, um anzugeben, ob während der Zugriffsauswertung eine zentrale Zugriffsrichtlinie verwendet werden soll.

</dd> <dt>

*ppCentralAccessPolicy* \[ out\]
</dt> <dd>

Zeiger auf die zentrale Zugriffsrichtlinie (Central Access Policy, CAP), die zum Auswerten des Zugriffs verwendet werden soll. Wenn dieser Wert **NULL** ist, wird die Standard-CAP angewendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt die Funktion **TRUE** zurück.

Wenn die Funktion die Auswertung nicht durchführen kann, gibt sie **FALSE** zurück. Verwenden Sie [**SetLastError,**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) um einen Fehler an die Zugriffsüberprüfungsfunktion zurückzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                   |
| Verteilbare Komponente<br/>          | Windows Server 2003 Administration Tools Pack auf Windows XP<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_AUTHZ-ZUGRIFFSANFORDERUNG \_**](/windows/desktop/api/Authz/ns-authz-authz_access_request)
</dt> <dt>

[**INIT-INFORMATIONEN ZU AUTHZ \_ \_**](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> </dl>

 

