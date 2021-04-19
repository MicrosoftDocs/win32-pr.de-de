---
description: Die authzgetcentralaccesspolicycallback-Funktion ist eine Anwendungs definierte Funktion, die die zentrale Zugriffs Richtlinie abruft. Authzgetcentralaccesspolicycallback ist ein Platzhalter für den Namen der Anwendungs definierten Funktion.
ms.assetid: 1D5831EF-ACA8-4EE9-A7C1-E1A3CB74CEC0
title: Authzgetcentralaccesspolicycallback-Rückruffunktion
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
ms.openlocfilehash: b96832fa647fde920a70ac3d6608c8ebb0048892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353225"
---
# <a name="authzgetcentralaccesspolicycallback-callback-function"></a>Authzgetcentralaccesspolicycallback-Rückruffunktion

Die *authzgetcentralaccesspolicycallback* -Funktion ist eine Anwendungs definierte Funktion, die die zentrale Zugriffs Richtlinie abruft. *Authzgetcentralaccesspolicycallback* ist ein Platzhalter für den Namen der Anwendungs definierten Funktion.

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

" *hauthzclientcontext* \[ " in\]
</dt> <dd>

Handle für den Client Kontext.

</dd> <dt>

*capid* \[ in\]
</dt> <dd>

Die ID der abzurufenden zentralen Zugriffs Richtlinie.

</dd> <dt>

 Argumente \[ in, optional\]
</dt> <dd>

Optionale Argumente, die über den **optionalarguments** -Member der [**Authz- \_ Zugriffs \_ Anforderungs**](/windows/desktop/api/Authz/ns-authz-authz_access_request) Struktur an die [**authzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) -Funktion übermittelt wurden.

</dd> <dt>

*pcentralaccesspolicyanwendbar* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen booleschen Wert, den der Ressourcen-Manager verwendet, um anzugeben, ob während der Zugriffs Auswertung eine zentrale Zugriffs Richtlinie verwendet werden soll.

</dd> <dt>

*ppcentralaccesspolicy* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die zentrale Zugriffs Richtlinie (Cap), die zum Auswerten des Zugriffs verwendet werden soll. Wenn dieser Wert **null** ist, wird die Standardgrenze angewendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion **true** zurück.

Wenn die Funktion die Auswertung nicht ausführen kann, wird **false** zurückgegeben. Verwenden Sie [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) , um einen Fehler an die Access Check-Funktion zurückzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                   |
| Verteilbare Komponente<br/>          | Windows Server 2003-Verwaltungs Tools Pack unter Windows XP<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Authz- \_ Zugriffs \_ Anforderung**](/windows/desktop/api/Authz/ns-authz-authz_access_request)
</dt> <dt>

[**Authz- \_ Init- \_ Informationen**](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[**Authzaccesscheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> </dl>

 

