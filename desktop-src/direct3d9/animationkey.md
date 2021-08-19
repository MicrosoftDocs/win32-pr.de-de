---
description: Definiert einen Satz von Animationsschlüsseln. Ein Matrixschlüssel ist nützlich für Gruppen von Animationsdaten, die als Transformationsmatrizen dargestellt werden müssen.
ms.assetid: bf007541-7fea-423e-910b-fa5f45271608
title: AnimationKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bad23a6cc519b0b0525cd0dac1b488184b3bf91e99359e252f44dca435ace529
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118806405"
---
# <a name="animationkey"></a>AnimationKey

Definiert einen Satz von Animationsschlüsseln. Ein Matrixschlüssel ist nützlich für Gruppen von Animationsdaten, die als Transformationsmatrizen dargestellt werden müssen.

``` syntax
template AnimationKey
{
    < 10DD46A8-775B-11CF-8F52-0040333594A3 >
    DWORD keyType;
    DWORD nKeys;
    array TimedFloatKeys keys[nKeys];
} 
```

Hierbei gilt:

-   keyType: Gibt an, ob es sich bei den Schlüsseln um Drehungs-, Skalierungs-, Positions- oder Matrixschlüssel handelt (mit den ganzen Zahlen 0, 1, 2 oder 3).
-   nKeys: Anzahl der Schlüssel.
-   keys: Ein Array von Schlüsseln. Siehe [**TimedFloatKeys.**](timedfloatkeys.md)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



