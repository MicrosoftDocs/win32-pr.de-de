---
description: Definiert einen Satz von Animations Schlüsseln. Ein Matrix Schlüssel ist nützlich für Sätze von Animationsdaten, die als Transformations Matrizen dargestellt werden müssen.
ms.assetid: bf007541-7fea-423e-910b-fa5f45271608
title: Animationkey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05728f124ae01962a1291547f8fe8b7fcebd175a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345452"
---
# <a name="animationkey"></a>Animationkey

Definiert einen Satz von Animations Schlüsseln. Ein Matrix Schlüssel ist nützlich für Sätze von Animationsdaten, die als Transformations Matrizen dargestellt werden müssen.

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

-   KeyType: gibt an, ob die Schlüssel Drehung, Skala, Position oder Matrix Schlüssel sind (mit den ganzen Zahlen 0, 1, 2 bzw. 3).
-   nkeys: Anzahl der Schlüssel.
-   Keys: ein Array von Schlüsseln. Weitere Informationen finden Sie unter [**timedfloatkeys**](timedfloatkeys.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



