---
description: Die authzfreecentralaccesspolicycallback-Funktion ist eine Anwendungs definierte Funktion, die von der authzgetcentralaccesspolicycallback-Funktion zugeordnete Arbeitsspeicher freigibt.
ms.assetid: F0859A67-4D20-4189-8F35-A78034E41E6A
title: Authzfreecentralaccesspolicycallback-Rückruffunktion
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
ms.openlocfilehash: d2139c9fa106b6070a3c043d417bdbf23379084b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218834"
---
# <a name="authzfreecentralaccesspolicycallback-callback-function"></a>Authzfreecentralaccesspolicycallback-Rückruffunktion

Die *authzfreecentralaccesspolicycallback* -Funktion ist eine Anwendungs definierte Funktion, die von der [*authzgetcentralaccesspolicycallback*](authzgetcentralaccesspolicycallback-.md) -Funktion zugeordnete Arbeitsspeicher freigibt. *Authzfreecentralaccesspolicycallback* ist ein Platzhalter für den Namen der Anwendungs definierten Funktion.

## <a name="syntax"></a>Syntax


```C++
BOOL CALLBACK AuthzFreeCentralAccessPolicyCallback(
  _In_ PVOID pCentralAccessPolicy
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcentralaccesspolicy* \[ in\]
</dt> <dd>

Ein Zeiger auf die zentrale Zugriffs Richtlinie, die freigegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion **true** zurück.

Wenn die Funktion die Auswertung nicht ausführen kann, wird **false** zurückgegeben. Verwenden Sie [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) , um einen Fehler an die Access Check-Funktion zurückzugeben.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Authz- \_ Init- \_ Informationen**](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[*Authzgetcentralaccesspolicycallback*](authzgetcentralaccesspolicycallback-.md)
</dt> </dl>

 

 
