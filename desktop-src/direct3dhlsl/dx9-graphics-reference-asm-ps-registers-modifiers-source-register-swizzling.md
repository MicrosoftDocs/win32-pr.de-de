---
title: Quellregister swizzling (HLSL PS-Referenz)
description: Swizzling bezieht sich auf die Möglichkeit, jede Quellregisterkomponente in eine beliebige temporäre Registerkomponente zu kopieren. Swizzling wirkt sich nicht auf die Quellregisterdaten aus. Bevor eine Anweisung ausgeführt wird, werden die Daten in einem Quellregister in ein temporäres Register kopiert.
ms.assetid: 27aee6a8-5185-4236-b3e4-44addf230c34
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2c0357a902c793165149da5c853ac953cf5989f8a472fe936c6c2b95cb9e3197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118090113"
---
# <a name="source-register-swizzling-hlsl-ps-reference"></a>Quellregister swizzling (HLSL PS-Referenz)

Swizzling bezieht sich auf die Möglichkeit, jede Quellregisterkomponente in eine beliebige temporäre Registerkomponente zu kopieren. Swizzling wirkt sich nicht auf die Quellregisterdaten aus. Bevor eine Anweisung ausgeführt wird, werden die Daten in einem Quellregister in ein temporäres Register kopiert.

## <a name="source-swizzling"></a>Quelle Swizzling

Quell-Swizzle ermöglicht es einzelnen Komponenten eines Quellregisters, den Wert einer der vier Komponenten desselben Quellregisters zu übernehmen, bevor das Register für die Berechnung gelesen wird.

Der ZXXY-Swizzle bedeutet beispielsweise Folgendes:

-   Die X-Komponente nimmt den Wert der Z-Komponente an.
-   Die .y-Komponente nimmt den Wert der X-Komponente an.
-   Die Z-Komponente nimmt den Wert der X-Komponente an.
-   Die W-Komponente nimmt den Wert der .y-Komponente an.

Die Komponenten können in beliebiger Reihenfolge angezeigt werden. Wenn weniger als vier Komponenten angegeben werden, wird die letzte Komponente wiederholt. Beispiel:


```
.xy  = .xyyy
.wzx = .wzxx
.z   = .zzzz
```



Wenn keine Komponente angegeben wird, wird kein Swizzling angewendet.

Einige Anweisungen enthalten Einschränkungen für Quell-Swizzle. Sie werden auf den referenzierten Anweisungsseiten aufgeführt.



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| .x                    |      |      |      | x    | x    | x    | x     | x    | x     |
| .y                    |      |      |      | x    | x    | x    | x     | x    | x     |
| .z                    | x\*  | x\*  | x\*  | x    | x    | x    | x     | x    | x     |
| .w                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| .xyzw (Standard)       | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| .yzxw                 |      |      |      |      | x    | x    | x     | x    | x     |
| .zxyw                 |      |      |      |      | x    | x    | x     | x    | x     |
| WZYX                 |      |      |      |      | x    | x    | x     | x    | x     |
| beliebiges Swizzle     |      |      |      |      |      | x    | x     | x    | x     |



 

\* Nur verfügbar, wenn die Ziel-Schreibmaske .w (.a) ist.

## <a name="arbitrary-swizzle"></a>Beliebiger Swizzle

Swizzles kann in beliebiger Reihenfolge auf Quellregister angewendet werden. Das heißt, jedes Quellregister kann eine beliebige Komponentenmaske in beliebiger Reihenfolge verwenden.

## <a name="replicate-swizzle"></a>Replizieren von Swizzle

Replizieren von Swizzle kopiert eine Komponente in eine andere. Dies bedeutet, dass genau eine der .x-, .y-, .z-, .w swizzle-Komponenten (oder die Entsprechungen .r, .g, .b, .a) angegeben werden muss.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Modifizierer für Das Pixel-Shader-Quellregister](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> <dt>

[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[ps \_ 2 \_ 0 Register](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[ps \_ 2 \_ x Register](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[ps \_ 3 \_ 0 Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




