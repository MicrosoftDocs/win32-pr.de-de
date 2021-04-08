---
title: Legacyauthenticationlevel
description: Legt die Standard Authentifizierungs Ebene für Anwendungen fest, die CoInitializeSecurity nicht aufzurufen.
ms.assetid: e14d2203-c84e-46af-befd-d82ef1936c9d
keywords:
- Legacyauthenticationlevel-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d87d808287418f635629e15324f2f517619be6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037612"
---
# <a name="legacyauthenticationlevel"></a>Legacyauthenticationlevel

Legt die Standard Authentifizierungs Ebene für Anwendungen fest, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht aufzurufen.

> [!Caution]  
> Es wird nicht empfohlen, diesen Wert zu ändern, da dies Auswirkungen auf alle com-Server Anwendungen hat, die nicht Ihre eigene Prozess weite Sicherheit festlegen, und möglicherweise verhindern, dass Sie ordnungsgemäß funktionieren. Wenn Sie diesen Wert ändern, um die Sicherheitseinstellungen für eine bestimmte COM-Anwendung zu beeinflussen, sollten Sie stattdessen die Prozess weiten Sicherheitseinstellungen für die jeweilige COM-Anwendung ändern. Weitere Informationen zum Festlegen der Prozess weiten Sicherheit finden Sie unter [Festlegen der Prozess weiten Sicherheit](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyAuthenticationLevel = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ Word** -Wert, der den Konstanten der RPC- \_ C- \_ authn- \_ Ebene entspricht.



| Wert | Konstante                             |
|-------|--------------------------------------|
| 1     | RPC- \_ C- \_ authn- \_ Ebene \_ None           |
| 2     | RPC- \_ C \_ authn \_ Level \_ Connect        |
| 3     | RPC- \_ C \_ authn-Ebene- \_ \_ Aufruf           |
| 4     | Pkt der RPC- \_ C- \_ authn- \_ Ebene \_            |
| 5     | \_Pkt-Integrität der RPC C- \_ authn- \_ Ebene \_ \_ |
| 6     | \_ \_ \_ \_ Pkt- \_ Datenschutz auf RPC-C-Ebene   |



 

Wenn dieser Registrierungs Wert nicht vorhanden ist, ist die vom System festgelegte Standard Authentifizierungs Ebene 2 (RPC \_ C \_ authn \_ Connect).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**AuthenticationLevel**](authenticationlevel.md)
</dt> <dt>

[Registrieren von com-Servern](registering-com-servers.md)
</dt> <dt>

[Festlegen der Prozess weiten Sicherheit](setting-processwide-security.md)
</dt> </dl>

 

 




