---
title: exp – im Vergleich zu
description: Stellt eine exponentielle 2-fache vollständige Genauigkeit bereit. | exp – im Vergleich zu
ms.assetid: 3644046b-3257-4257-9880-146ca50f6b0b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2b5b27067e83cbfd7604165ec1191d3371634aac15781a719377c92c69e29e6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067950"
---
# <a name="exp---vs"></a>exp – im Vergleich zu

Stellt exponentielle 2<sup>x</sup>volle Genauigkeit bereit.

## <a name="syntax"></a>Syntax



| exp dst, src |
|--------------|



 

where

-   dst ist das Zielregister.
-   src ist ein Quellregister. Das Quellregister erfordert die explizite Verwendung von replicate swizzle, d.h., dass genau eine der .x-, .y-, .z-, W-Swizzle-Komponenten (oder die Entsprechungen .r, .g, .b, .a) angegeben werden muss. Weitere Informationen finden Sie [unter Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md).

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| exp                    | x    | x    | x    | x     | x    | x     |



 

Diese Anweisung bietet mindestens 21 Bit Genauigkeit.

Das folgende Codefragment zeigt die ausgeführten Vorgänge:


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




