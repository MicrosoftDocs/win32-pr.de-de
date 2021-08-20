---
title: LegacyImpersonationLevel
description: Legt die Standardebene des Identitätswechsels für Anwendungen fest, die CoInitializeSecurity nicht aufrufen.
ms.assetid: 3f42c6d7-729d-4406-9391-4bfe28f7a59d
keywords:
- LegacyImpersonationLevel-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd032e83290c18fc3a2588e382ade7730fa2ea39a7847e375b1e887cdbbb90f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048078"
---
# <a name="legacyimpersonationlevel"></a>LegacyImpersonationLevel

Legt die Standardebene des Identitätswechsels für Anwendungen fest, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht aufrufen.

> [!Caution]  
> Es wird nicht empfohlen, diesen Wert zu ändern, da sich dies auf alle COM-Serveranwendungen auswirkt, die keine eigene prozessweite Sicherheit festlegen und möglicherweise verhindern, dass sie ordnungsgemäß funktionieren. Wenn Sie diesen Wert ändern, um die Sicherheitseinstellungen für eine bestimmte COM-Anwendung zu beeinflussen, sollten Sie stattdessen die prozessweiten Sicherheitseinstellungen für diese bestimmte COM-Anwendung ändern. Weitere Informationen zum Festlegen der prozessweiten Sicherheit finden Sie unter [Festlegen der prozessweiten Sicherheit.](setting-processwide-security.md)

 

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyImpersonationLevel = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ WORD-Wert,** der den RPC \_ \_ C-IMP \_ LEVEL-Konstanten entspricht.



| Wert | Konstante                        |
|-------|---------------------------------|
| 1     | RPC \_ C \_ IMP \_ LEVEL \_ ANONYMOUS   |
| 2     | RPC \_ C \_ IMP \_ LEVEL \_ IDENTIFY    |
| 3     | RPC \_ C \_ IMP \_ LEVEL \_ IMPERSONATE |
| 4     | RPC \_ C \_ IMP \_ LEVEL \_ DELEGATE    |



 

Wenn dieser Registrierungswert nicht vorhanden ist, ist die vom System festgelegte Standardidentitätsebene 2 (RPC \_ C \_ IMP \_ LEVEL \_ IDENTIFY).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von COM-Servern](registering-com-servers.md)
</dt> <dt>

[Festlegen der prozessweiten Sicherheit](setting-processwide-security.md)
</dt> </dl>

 

 




