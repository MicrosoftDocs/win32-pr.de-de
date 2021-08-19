---
description: Die Funktion "AuhzFreeCentralAccessPolicyCallback" ist eine anwendungsdefinierte Funktion, die den von der Funktion "SollhzGetCentralAccessPolicyCallback" zugewiesenen Arbeitsspeicher frei gibt.
ms.assetid: F0859A67-4D20-4189-8F35-A78034E41E6A
title: Rückruffunktion "HzFreeCentralAccessPolicyCallback"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: f51903708bd3993e2837d65107798b1ff546c5857eff3bbed028ed4d6dda47f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783754"
---
# <a name="authzfreecentralaccesspolicycallback-callback-function"></a>Rückruffunktion "HzFreeCentralAccessPolicyCallback"

Die *Funktion "AuhzFreeCentralAccessPolicyCallback"* ist eine anwendungsdefinierte Funktion, die den von der [*Funktion "SollhzGetCentralAccessPolicyCallback"*](authzgetcentralaccesspolicycallback-.md) zugewiesenen Arbeitsspeicher frei gibt. *HzFreeCentralAccessPolicyCallback* ist ein Platzhalter für den anwendungsdefinierten Funktionsnamen.

## <a name="syntax"></a>Syntax


```C++
BOOL CALLBACK AuthzFreeCentralAccessPolicyCallback(
  _In_ PVOID pCentralAccessPolicy
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCentralAccessPolicy* \[ In\]
</dt> <dd>

Zeiger auf die zentrale Zugriffsrichtlinie, die frei werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt die Funktion **TRUE zurück.**

Wenn die Funktion die Auswertung nicht ausführen kann, gibt sie **FALSE zurück.** Verwenden [**Sie SetLastError,**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) um einen Fehler an die Zugriffsüberprüfungsfunktion zurück zu geben.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_INIT-INFORMATIONEN ZUHZ \_**](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[*HzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md)
</dt> </dl>

 

 
