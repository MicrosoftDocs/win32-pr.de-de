---
title: Srpactivateasactivatorchecks
description: Bestimmt, ob die Richtlinien für die Software Einschränkungs Richtlinie (SRP) während der Aktivierungen von activateasactivator verwendet werden.
ms.assetid: b0d616c3-1cb0-4854-a4f9-6635d61b0698
keywords:
- Srpactivateasactivatorchecks-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b66ae6b1c7f267f48f24441c04e95eea75e4345
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709432"
---
# <a name="srpactivateasactivatorchecks"></a>Srpactivateasactivatorchecks

Bestimmt, ob die Richtlinien für die Software Einschränkungs Richtlinie (SRP) während der Aktivierungen von activateasactivator verwendet werden.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPActivateAsActivatorChecks = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ SZ** -Wert.

Zeichen folgen Werte ({N, n, Nein, Nein, Nein}) geben an, dass das Server Objekt mit der SRP-Vertrauens Ebene des Client Objekts ausgeführt wird, unabhängig von der SRP-Vertrauens Ebene, mit der es konfiguriert wurde. Wenn dieser Registrierungs Wert auf einen anderen Wert festgelegt ist oder nicht vorhanden ist, wird die für das Server Objekt konfigurierte SRP-Vertrauens Ebene mit der SRP-Vertrauens Ebene des Client Objekts verglichen, und es wird die strengere Vertrauens Ebene zum Ausführen des Server Objekts verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SRPTrustLevel](srptrustlevel.md)
</dt> </dl>

 

 




