---
title: MiscStatus
description: Gibt an, wie ein Objekt erstellt und angezeigt wird.
ms.assetid: 585b2d1e-3edb-494e-a61e-bbfa6eae2ba1
keywords:
- MiscStatus-Registrierungsschlüssel-COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41aa5a5ab7f777eb6aa19d919c69ca219c9364cd1d6e5e9471cb677300d4ebb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992350"
---
# <a name="miscstatus"></a>MiscStatus

Gibt an, wie ein Objekt erstellt und angezeigt wird.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      MiscStatus
         (Default) = value
         aspect = value
```

## <a name="remarks"></a>Hinweise

Weitere Informationen finden Sie unter der [**OLEMISC-Enumeration**](/windows/win32/api/oleidl/ne-oleidl-olemisc) und [**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).

Wenn kein Unterschlüssel gefunden wird, der einem DVASPECT entspricht, wird der Standardwert **MiscStatus** verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus)
</dt> </dl>

 

 




