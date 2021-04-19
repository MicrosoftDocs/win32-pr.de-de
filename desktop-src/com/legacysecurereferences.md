---
title: Legacysecurereferences
description: Bestimmt, ob adressf/releaseaufrufe für Anwendungen gesichert werden, die CoInitializeSecurity nicht aufrufen.
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- Legacysecurereferences-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2776bf3661013f1e622bbc2e1c553f2551c62808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341863"
---
# <a name="legacysecurereferences"></a>Legacysecurereferences

Bestimmt, ob **adressf**- / **releaseaufrufe** für Anwendungen gesichert werden, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht aufrufen.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacySecureReferences = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ SZ** -Wert. Der Wert "y" oder "y" zeigt an, dass **adressf** und **Release** gesichert sind. Wenn dieser Registrierungs Wert nicht vorhanden ist oder auf einen anderen Wert als ' y ' oder ' y ' festgelegt ist, werden **adressf** und **Release** nicht gesichert. Durch das Aktivieren sicherer Verweise werden Remote Aufrufe verlangsamt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von com-Servern](registering-com-servers.md)
</dt> <dt>

[Festlegen der Prozess weiten Sicherheit](setting-processwide-security.md)
</dt> </dl>

 

 




