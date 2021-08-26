---
description: Ermöglicht das Festlegen von Animationsoptionen.
ms.assetid: 727b4d87-4164-4915-b158-d21fe7d1b729
title: AnimationOptions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 346eaa1b94637fa357f09cd701ac9d99d5ddf2076ee12654076e54bce82527fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069430"
---
# <a name="animationoptions"></a>AnimationOptions

Ermöglicht das Festlegen von Animationsoptionen.

``` syntax
template AnimationOptions
{
    < E2BF56C0-840F-11cf-8F52-0040333594A3 >
    DWORD openclosed;
    DWORD positionquality;
} 
```

Hierbei gilt:

-   openclosed: Verwenden Sie 0 für eine geschlossene Animation oder 1 für eine geöffnete Animation. Standardmäßig wird eine Animation geschlossen.
-   positionquality: Legen Sie die Positionsqualität für alle angegebenen Positionsschlüssel fest. Verwenden Sie 0 für Splinepositionen oder 1 für lineare Positionen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



