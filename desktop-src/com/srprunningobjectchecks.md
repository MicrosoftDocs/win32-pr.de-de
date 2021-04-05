---
title: Srprunningobjectchecks
description: Bestimmt, ob Verbindungsversuche mit ausgelaufenden Objekten auf kompatible Richtlinien für Software Einschränkungs Richtlinien (SRP) überprüft werden.
ms.assetid: ab5e74f0-d167-4fb2-af1b-03704039e87c
keywords:
- Srprunningobjectchecks-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ad307856bcfdd30cfaa6c731551ac6570d2bec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709431"
---
# <a name="srprunningobjectchecks"></a>Srprunningobjectchecks

Bestimmt, ob Verbindungsversuche mit ausgelaufenden Objekten auf kompatible Richtlinien für Software Einschränkungs Richtlinien (SRP) überprüft werden.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPRunningObjectChecks = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ SZ** -Wert.

Zeichen folgen Werte ({N, n, Nein, Nein, Nein}) geben an, dass Verbindungsversuche mit ausgelaufenden Objekten nicht auf kompatible SRP-Vertrauens Ebenen überprüft werden. Wenn dieser Registrierungs Wert auf einen anderen Wert festgelegt ist oder nicht vorhanden ist, kann das laufende Objekt nicht über eine weniger strenge SRP-Vertrauens Ebene verfügen als das Client Objekt. Beispielsweise kann das laufende Objekt nicht über eine unzulässige Vertrauens Ebene verfügen, wenn das Client Objekt eine uneingeschränkte Vertrauens Ebene aufweist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SRPTrustLevel](srptrustlevel.md)
</dt> </dl>

 

 




