---
title: Control
description: Identifiziert ein Objekt als ActiveX-Steuerelement.
ms.assetid: 2487e642-1d21-4811-87dd-b280be98a44b
keywords:
- Registrierungsschlüssel-com Steuern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3722d85b38399d7e95f226749bda45ccc82d1369
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388750"
---
# <a name="control"></a>Control

Identifiziert ein Objekt als ActiveX-Steuerelement.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a>Bemerkungen

Dieser optionale Eintrag wird von Containern zum Ausfüllen von Dialogfeldern verwendet. Der Container verwendet diesen Unterschlüssel, um zu bestimmen, ob ein Objekt in ein Dialogfeld eingeschlossen werden soll, das ActiveX-Steuerelemente anzeigt. Ein Steuerelement kann diesen Eintrag weglassen, wenn er nur für den Einsatz mit einem bestimmten Container vorgesehen ist und daher nicht in anderen Containern eingefügt werden soll.

 

 




