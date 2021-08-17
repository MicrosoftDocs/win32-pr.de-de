---
title: AuxUserType
description: Gibt den kurzen Anzeigenamen und die Anwendungsnamen einer Anwendung an.
ms.assetid: 3367eb68-01f4-4cb9-b1d0-27554c28b68d
keywords:
- AuxUserType-Registrierungsschlüssel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1dbec8e873e6f6cfcb5fdb29468c1f09c0a7a6935280054e129ddac0b49e282
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550719"
---
# <a name="auxusertype"></a>AuxUserType

Gibt den kurzen Anzeigenamen und die Anwendungsnamen einer Anwendung an.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AuxUserType
         2 = ShortDisplayName
         3 = ApplicationName
```

## <a name="remarks"></a>Hinweise

Die empfohlene maximale Länge für *ShortDisplayName* beträgt 15 Zeichen. Dieser Name wird in Menüs verwendet, einschließlich Popupmenüs.

*ApplicationName* sollte den tatsächlichen Namen der Anwendung enthalten (z.B. "Acme Draw 2.0"). Dieser Name wird im Feld **Ergebnisse** des Dialogfelds **Spezielle** Einfügen verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> </dl>

 

 




