---
title: Fehlstatus
description: Gibt an, wie ein Objekt erstellt und angezeigt wird.
ms.assetid: 585b2d1e-3edb-494e-a61e-bbfa6eae2ba1
keywords:
- Falsch Status-Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abee49776577df61dc8b7d4e94a0621dfdd8b216
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037190"
---
# <a name="miscstatus"></a>Fehlstatus

Gibt an, wie ein Objekt erstellt und angezeigt wird.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      MiscStatus
         (Default) = value
         aspect = value
```

## <a name="remarks"></a>Bemerkungen

Weitere Informationen finden Sie unter [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) -Enumeration und [**IOleObject:: getfehlstatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).

Wenn kein Unterschlüssel gefunden wird, der einem DVASPECT entspricht, wird der Standardwert von " **fehlstatus** " verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IOleObject:: getfehlstatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus)
</dt> </dl>

 

 




