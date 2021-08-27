---
title: LegacyAuthenticationLevel
description: Legt die Standardauthentifizierungsebene für Anwendungen fest, die CoInitializeSecurity nicht aufrufen.
ms.assetid: e14d2203-c84e-46af-befd-d82ef1936c9d
keywords:
- LegacyAuthenticationLevel-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6be9f562a543e4750695ec2bf967b5a261209aae70d0bf91269bc2a074a9e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096950"
---
# <a name="legacyauthenticationlevel"></a>LegacyAuthenticationLevel

Legt die Standardauthentifizierungsebene für Anwendungen fest, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht aufrufen.

> [!Caution]  
> Es wird nicht empfohlen, diesen Wert zu ändern, da sich dies auf alle COM-Serveranwendungen auswirkt, die keine eigene prozessweite Sicherheit festlegen und möglicherweise verhindern, dass sie ordnungsgemäß funktionieren. Wenn Sie diesen Wert ändern, um die Sicherheitseinstellungen für eine bestimmte COM-Anwendung zu beeinflussen, sollten Sie stattdessen die prozessweiten Sicherheitseinstellungen für diese bestimmte COM-Anwendung ändern. Weitere Informationen zum Festlegen der prozessweiten Sicherheit finden Sie unter [Festlegen der prozessweiten Sicherheit.](setting-processwide-security.md)

 

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyAuthenticationLevel = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ WORD-Wert,** der den RPC \_ \_ \_ C-AUTHN LEVEL-Konstanten entspricht.



| Wert | Konstante                             |
|-------|--------------------------------------|
| 1     | RPC \_ C \_ AUTHN \_ LEVEL \_ NONE           |
| 2     | RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT        |
| 3     | RPC \_ \_ \_ C-AUFRUF AUF AUTHENTIFIZIERUNGSEBENE \_           |
| 4     | RPC \_ C \_ AUTHN \_ LEVEL \_ PKT            |
| 5     | \_ \_ \_ \_ PKT-INTEGRITÄT AUF RPC-C-AUTHENTIFIZIERUNGSEBENE \_ |
| 6     | RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY   |



 

Wenn dieser Registrierungswert nicht vorhanden ist, ist die vom System festgelegte Standardauthentifizierungsebene 2 (RPC \_ C \_ AUTHN \_ CONNECT).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Authenticationlevel**](authenticationlevel.md)
</dt> <dt>

[Registrieren von COM-Servern](registering-com-servers.md)
</dt> <dt>

[Festlegen der prozessweiten Sicherheit](setting-processwide-security.md)
</dt> </dl>

 

 




