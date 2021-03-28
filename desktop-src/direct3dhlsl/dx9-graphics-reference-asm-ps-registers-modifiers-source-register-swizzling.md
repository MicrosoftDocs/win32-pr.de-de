---
title: Quellen Register (swizzelnder) (HLSL PS-Referenz)
description: Swizzling bezieht sich auf die Möglichkeit, beliebige Quell Registrierungs Komponenten in beliebige temporäre Register Komponenten zu kopieren. Das Schwenken wirkt sich nicht auf die Quell Registrierungsdaten aus. Bevor eine Anweisung ausgeführt wird, werden die Daten in einem Quell Register in ein temporäres Register kopiert.
ms.assetid: 27aee6a8-5185-4236-b3e4-44addf230c34
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ffc655129740f112a3ade9eb40c0bbe29dfc1fb
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104313793"
---
# <a name="source-register-swizzling-hlsl-ps-reference"></a>Quellen Register (swizzelnder) (HLSL PS-Referenz)

Swizzling bezieht sich auf die Möglichkeit, beliebige Quell Registrierungs Komponenten in beliebige temporäre Register Komponenten zu kopieren. Das Schwenken wirkt sich nicht auf die Quell Registrierungsdaten aus. Bevor eine Anweisung ausgeführt wird, werden die Daten in einem Quell Register in ein temporäres Register kopiert.

## <a name="source-swizzling"></a>Quellen Schwimmen

Quell-wischen ermöglicht es einer einzelnen Komponente eines Quell Registers, den Wert einer der vier Komponenten des gleichen Quell Registers zu übernehmen, bevor das Register für die Berechnung gelesen wird.

Beispielsweise bedeutet das. zxxy-Swizzle:

-   . x-Komponente übernimmt den Wert der. z-Komponente.
-   . y-Komponente übernimmt den Wert der x-Komponente.
-   . z-Komponente übernimmt den Wert der x-Komponente.
-   . w-Komponente übernimmt den Wert der. y-Komponente.

Die Komponenten können in beliebiger Reihenfolge angezeigt werden. Wenn weniger als vier Komponenten angegeben werden, wird die letzte Komponente wiederholt. Beispiel:


```
.xy  = .xyyy
.wzx = .wzxx
.z   = .zzzz
```



Wenn keine Komponente angegeben ist, wird kein schwenken angewendet.

Einige Anweisungen weisen Einschränkungen für den Quellpfad auf. Sie sind auf den Referenzseiten der angesehenen Anweisung aufgeführt.



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| .x                    |      |      |      | x    | x    | x    | x     | x    | x     |
| . y                    |      |      |      | x    | x    | x    | x     | x    | x     |
| . z                    | x\*  | x\*  | x\*  | x    | x    | x    | x     | x    | x     |
| . w                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| . xyzw (Standard)       | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| . yzxw                 |      |      |      |      | x    | x    | x     | x    | x     |
| . zxyw                 |      |      |      |      | x    | x    | x     | x    | x     |
| wzyx-Datei                 |      |      |      |      | x    | x    | x     | x    | x     |
| beliebiger Swizzle     |      |      |      |      |      | x    | x     | x    | x     |



 

\* Nur verfügbar, wenn die Ziel Schreib Maske. w (. a) ist.

## <a name="arbitrary-swizzle"></a>Beliebiger Swizzle

Auf Quell Register können in beliebiger Reihenfolge Streifen angewendet werden. Das heißt, jedes Quell Register kann jede beliebige Komponenten Maske in beliebiger Reihenfolge verwenden.

## <a name="replicate-swizzle"></a>Flüchtigen Replikat

Replizieren von Swizzle kopiert eine Komponente in eine andere. Dies ist genau eine der. x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-Entsprechungen) müssen angegeben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel-Shader-quellregistrierungs Modifizierern](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> <dt>

[PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 Register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[PS \_ 2 \_ 0-Register](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[PS \_ 2 \_ x-Register](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[PS \_ 3 \_ 0-Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




