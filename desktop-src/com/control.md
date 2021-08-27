---
title: Control
description: Identifiziert ein Objekt als ActiveX-Steuerelement.
ms.assetid: 2487e642-1d21-4811-87dd-b280be98a44b
keywords:
- Steuern des Registrierungsschlüssel-COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03aa6a0b131dd5fc2ba10d9aaeabafd06b19b73bb1e9422c28e5bec45ea43cbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120510"
---
# <a name="control"></a>Control

Identifiziert ein Objekt als ActiveX-Steuerelement.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a>Hinweise

Dieser optionale Eintrag wird von Containern zum Ausfüllen von Dialogfeldern verwendet. Der Container verwendet diesen Unterschlüssel, um zu bestimmen, ob ein Objekt in ein Dialogfeld eingeschlossen werden soll, das ActiveX Controls anzeigt. Ein Steuerelement kann diesen Eintrag weglassen, wenn es nur für die Verwendung mit einem bestimmten Container konzipiert ist und daher nicht für das Einfügen in andere Container vorgesehen ist.

 

 




