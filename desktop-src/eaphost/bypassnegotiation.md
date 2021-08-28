---
title: BypassNegotiation
description: Der BypassNegotiation-Registrierungsschlüssel bestimmt, ob die Aushandlung von Funktionen zwischen dem Server und dem Client erfolgt oder ob vorkonfigurierte Einstellungen verwendet werden.
ms.assetid: 51e21e9c-d6cb-454b-9584-3f48d76a649a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ba914b9c1ec1d5e3caef6b86ddbda49d021268e456c877ff4f67db86efd2cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978250"
---
# <a name="bypassnegotiation"></a>BypassNegotiation

Der BypassNegotiation-Registrierungsschlüssel bestimmt, ob die Aushandlung von Funktionen zwischen dem Server und dem Client erfolgt oder ob vorkonfigurierte Einstellungen verwendet werden.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   BypassNegotiation = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ DWORD-Wert.**



| Wert   | Beschreibung                                                                                                                                                                                          |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0       | Server- und Client-Negotiate-EAP-Funktionen.                                                                                                                                                        |
| Nonzero | Server und Client handeln keine EAP-Funktionen aus. Server und Client verwenden den Registrierungsschlüsselwert [AssumePhase2Fragmentation,](assumephase2fragmentation.md) um die Funktionen der anderen Partei zu ermitteln. |



 

Wenn dieser Registrierungswert nicht vorhanden ist, handeln der Server und der Client EAP-Funktionen aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost Registry Einstellungen](eaphost-registry-settings.md)
</dt> </dl>

 

 




