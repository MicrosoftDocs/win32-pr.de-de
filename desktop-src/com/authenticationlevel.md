---
title: AuthenticationLevel
description: Legt die Authentifizierungs Ebene für Anwendungen fest, die CoInitializeSecurity nicht aufzurufen, oder für Anwendungen, die CoInitializeSecurity anrufen und eine AppID angeben.
ms.assetid: 137cbffe-6f45-43f4-bf35-b064b3607fcc
keywords:
- Registrierungs Wert "AuthenticationLevel" com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b04bcf4992c8a6943bcb515fa0a4eae616fec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311507"
---
# <a name="authenticationlevel"></a>AuthenticationLevel

Legt die Authentifizierungs Ebene für Anwendungen fest, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) nicht aufzurufen, oder für Anwendungen, die **CoInitializeSecurity** anrufen und eine AppID angeben.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AuthenticationLevel = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ DWORD** -Wert, der den Konstanten der RPC- \_ C- \_ authn- \_ Ebene entspricht.



| Wert | Konstante                             |
|-------|--------------------------------------|
| 1     | RPC- \_ C- \_ authn- \_ Ebene \_ None           |
| 2     | RPC- \_ C \_ authn \_ Level \_ Connect        |
| 3     | RPC- \_ C \_ authn-Ebene- \_ \_ Aufruf           |
| 4     | Pkt der RPC- \_ C- \_ authn- \_ Ebene \_            |
| 5     | \_Pkt-Integrität der RPC C- \_ authn- \_ Ebene \_ \_ |
| 6     | \_ \_ \_ \_ Pkt- \_ Datenschutz auf RPC-C-Ebene   |



 

Der Wert **AuthenticationLevel** ähnelt dem Wert von [**legacyauthenticationlevel**](legacyauthenticationlevel.md) . Wenn der **AuthenticationLevel** -Wert vorhanden ist, wird er anstelle des **legacyauthenticationlevel** -Werts für diese AppID verwendet.

Wenn der **AuthenticationLevel** -Wert vom falschen Typ oder außerhalb des gültigen Bereichs ist, schlägt [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) fehl, wodurch das Marshalling der Schnittstelle fehlschlägt. Dadurch wird verhindert, dass die Anwendung überhaupt Aufrufe durchführen kann (Apartment übergreifend, Thread übergreifend, Prozess übergreifend oder Computer übergreifend).

Die Werte " **AuthenticationLevel** " und " [**AccessPermission**](accesspermission.md) " sind unabhängig voneinander. Wenn kein Wert vorhanden ist, wird der Standardwert verwendet. In den folgenden Regeln wird die Interaktion zwischen dem Wert **AuthenticationLevel** und dem **AccessPermission** -Wert aufgeführt:

-   Wenn **AuthenticationLevel** den Wert None hat, werden die Werte [**AccessPermission**](accesspermission.md) und [**DefaultAccessPermission**](defaultaccesspermission.md) ignoriert (für diese Anwendung).
-   Wenn " **AuthenticationLevel** " nicht vorhanden ist und " [**legacyauthenticationlevel**](legacyauthenticationlevel.md) " auf "None" festgelegt ist, werden die Werte [**AccessPermission**](accesspermission.md) und [**DefaultAccessPermission**](defaultaccesspermission.md) ignoriert (für diese Anwendung).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konstanten auf Authentifizierungs Ebene](com-authentication-level-constants.md)
</dt> <dt>

[**Legacyauthenticationlevel**](legacyauthenticationlevel.md)
</dt> <dt>

[Registrieren von com-Servern](registering-com-servers.md)
</dt> <dt>

[Sicherheit in com](security-in-com.md)
</dt> </dl>

 

 




