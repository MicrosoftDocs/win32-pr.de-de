---
title: SRPRunningObjectChecks
description: Bestimmt, ob Versuche, eine Verbindung mit ausgeführten Objekten herzustellen, auf kompatible Vertrauensebenen der Softwareeinschränkungsrichtlinie (Software Restriction Policy, SRP) überprüft werden.
ms.assetid: ab5e74f0-d167-4fb2-af1b-03704039e87c
keywords:
- SRPRunningObjectChecks-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c416b5f430540282873e37c5e74ef2cccc1c564f4a5b27842ba2a49e99cc8769
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129792"
---
# <a name="srprunningobjectchecks"></a>SRPRunningObjectChecks

Bestimmt, ob Versuche, eine Verbindung mit ausgeführten Objekten herzustellen, auf kompatible Vertrauensebenen der Softwareeinschränkungsrichtlinie (Software Restriction Policy, SRP) überprüft werden.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPRunningObjectChecks = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ SZ-Wert.**

Die Zeichenfolgenwerte {N, n, NO, No, no} geben an, dass Versuche, eine Verbindung mit ausgeführten Objekten herzustellen, nicht auf kompatible SRP-Vertrauensebenen überprüft werden. Wenn dieser Registrierungswert auf einen anderen Wert festgelegt ist oder nicht vorhanden ist, kann das ausgeführte Objekt keine weniger strenge SRP-Vertrauensebene als das Clientobjekt aufweisen. Beispielsweise kann das ausgeführte Objekt keine Unzulässige Vertrauensebene aufweisen, wenn das Clientobjekt über eine uneingeschränkte Vertrauensebene verfügt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SRPTrustLevel](srptrustlevel.md)
</dt> </dl>

 

 




