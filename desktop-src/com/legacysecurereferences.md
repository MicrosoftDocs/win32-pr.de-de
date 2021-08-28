---
title: LegacySecureReferences
description: Bestimmt, ob AddRef/Release-Aufrufe für Anwendungen geschützt sind, die CoInitializeSecurity nicht aufrufen.
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- LegacySecureReferences-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3a4ab964d73fa4b194c734f28c23ff068239370088c090051464129b6caf14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736547"
---
# <a name="legacysecurereferences"></a>LegacySecureReferences

Bestimmt, ob **AddRef** / **Release-Aufrufe** für Anwendungen geschützt sind, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht aufrufen.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacySecureReferences = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ SZ-Wert.** Der Wert "Y" oder "y" gibt an, dass **AddRef** und **Release** gesichert sind. Wenn dieser Registrierungswert nicht vorhanden ist oder auf einen anderen Wert als "Y" oder "y" festgelegt ist, werden **AddRef** und **Release** nicht gesichert. Durch das Aktivieren sicherer Verweise werden Remoteaufrufe verlangsamt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von COM-Servern](registering-com-servers.md)
</dt> <dt>

[Festlegen der prozessweiten Sicherheit](setting-processwide-security.md)
</dt> </dl>

 

 




