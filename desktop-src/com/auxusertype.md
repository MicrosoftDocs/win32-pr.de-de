---
title: "\"Auxusertype\""
description: Gibt den kurzen anzeigen Amen und Anwendungsnamen einer Anwendung an.
ms.assetid: 3367eb68-01f4-4cb9-b1d0-27554c28b68d
keywords:
- Registrierungsschlüssel für "auxusertype" com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c66fcfbcdc2886e93d08040659b39c42d47c291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707032"
---
# <a name="auxusertype"></a>"Auxusertype"

Gibt den kurzen anzeigen Amen und Anwendungsnamen einer Anwendung an.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AuxUserType
         2 = ShortDisplayName
         3 = ApplicationName
```

## <a name="remarks"></a>Bemerkungen

Die empfohlene maximale Länge für *ShortDisplayName* beträgt 15 Zeichen. Dieser Name wird in Menüs wie Popup Menüs verwendet.

*ApplicationName* muss den tatsächlichen Namen der Anwendung enthalten (z. b. "Acme Draw 2,0"). Dieser Name wird im **Ergebnis** Feld des Dialog Felds " **spezielles einfügen** " verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> </dl>

 

 




