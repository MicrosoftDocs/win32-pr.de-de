---
title: Authenticationlevel
description: Legt die Authentifizierungsebene für Anwendungen fest, die CoInitializeSecurity nicht aufrufen, oder für Anwendungen, die CoInitializeSecurity aufrufen und eine AppID angeben.
ms.assetid: 137cbffe-6f45-43f4-bf35-b064b3607fcc
keywords:
- AuthenticationLevel-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7968382ea97243c1116dd6785be34a0d1c3e6eafc6cb9ee13f16b939029a6611
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120530"
---
# <a name="authenticationlevel"></a>Authenticationlevel

Legt die Authentifizierungsebene für Anwendungen fest, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) nicht aufrufen, oder für Anwendungen, die **CoInitializeSecurity** aufrufen und eine AppID angeben.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AuthenticationLevel = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ DWORD-Wert,** der den RPC \_ C \_ AUTHN \_ LEVEL-Konstanten entspricht.



| Wert | Konstante                             |
|-------|--------------------------------------|
| 1     | RPC \_ C \_ AUTHN \_ LEVEL \_ NONE           |
| 2     | RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT        |
| 3     | RPC \_ \_ \_ C-AUFRUF AUF AUTHENTIFIZIERUNGSEBENE \_           |
| 4     | RPC \_ C \_ AUTHN \_ LEVEL \_ PKT            |
| 5     | \_ \_ \_ \_ PKT-INTEGRITÄT AUF RPC-C-AUTHENTIFIZIERUNGSEBENE \_ |
| 6     | RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY   |



 

Der **AuthenticationLevel-Wert** ähnelt dem [**LegacyAuthenticationLevel-Wert.**](legacyauthenticationlevel.md) Wenn der **AuthenticationLevel-Wert** vorhanden ist, wird er anstelle des **LegacyAuthenticationLevel-Werts** für diese AppID verwendet.

Wenn der **AuthenticationLevel-Wert** den falschen Typ auf oder außerhalb des Bereichs hat, schlägt [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) fehl, was zu einem Fehler beim Marshalling der Schnittstelle führt. Dadurch wird verhindert, dass die Anwendung überhaupt Aufrufe (apartmentübergreifend, threadübergreifend, prozessübergreifend oder computerübergreifend) vornimmt.

Die Werte **AuthenticationLevel** und [**AccessPermission**](accesspermission.md) sind unabhängig. Wenn keine vorhanden ist, wird der Standardwert verwendet. Die folgenden Regeln listen die Interaktion zwischen dem **AuthenticationLevel-Wert** und dem **AccessPermission-Wert** auf:

-   Wenn **AuthenticationLevel** NONE ist, werden die Werte [**AccessPermission**](accesspermission.md) und [**DefaultAccessPermission**](defaultaccesspermission.md) (für diese Anwendung) ignoriert.
-   Wenn **AuthenticationLevel** nicht vorhanden ist und [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) NONE ist, werden die Werte [**AccessPermission**](accesspermission.md) und [**DefaultAccessPermission**](defaultaccesspermission.md) (für diese Anwendung) ignoriert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konstanten auf Authentifizierungsebene](com-authentication-level-constants.md)
</dt> <dt>

[**LegacyAuthenticationLevel**](legacyauthenticationlevel.md)
</dt> <dt>

[Registrieren von COM-Servern](registering-com-servers.md)
</dt> <dt>

[Sicherheit in COM](security-in-com.md)
</dt> </dl>

 

 




