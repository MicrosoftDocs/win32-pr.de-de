---
description: Ermöglicht es Ihnen, Animations Optionen festzulegen.
ms.assetid: 727b4d87-4164-4915-b158-d21fe7d1b729
title: AnimationOptions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7bd3c5df8081523ccef2a802e631454fadaeeae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127129"
---
# <a name="animationoptions"></a>AnimationOptions

Ermöglicht es Ihnen, Animations Optionen festzulegen.

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
-   positionquality: legt die Positions Qualität für beliebige Positions Schlüssel fest. Verwenden Sie 0 für Spline-Positionen oder 1 für lineare Positionen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



