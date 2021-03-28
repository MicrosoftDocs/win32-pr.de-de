---
title: break_comp-PS
description: Unterbrechen Sie die aktuelle Schleife bei den nächstgelegenen ENDLOOP-PS oder ENDREP-PS, basierend auf einem pro-Komponente-Vergleich.
ms.assetid: d21e850f-05db-4a29-b15b-85bb1c1410d0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5088312a16102153ad78afffdcd9ea1275d34e0d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101086"
---
# <a name="break_comp---ps"></a>\_Comp-PS Abbrechen

Unterbrechen Sie die aktuelle Schleife bei den nächstgelegenen [ENDLOOP-PS](endloop---ps.md) oder [ENDREP-PS](endrep---ps.md), basierend auf einem pro-Komponente-Vergleich.

## <a name="syntax"></a>Syntax



| Break \_ Comp src0, Quelle1 |
|------------------------|



 

Hierbei gilt:

-   \_comp ist ein skalarer (oder einzelner) Vergleich zwischen den beiden Quell Registern. Folgende Werte sind möglich: 

    | Syntax | Vergleich            |
    |--------|-----------------------|
    | \_siegt   | Größer als          |
    | \_General   | Kleiner als             |
    | \_Färbung   | Größer als oder gleich |
    | \_Kirchturm   | Kleiner als oder gleich    |
    | \_stecken   | Gleich              |
    | \_NES   | Ungleich          |

    

     

-   src0 ist ein Quell Register. Bei der Auswahl einer einzelnen Komponente ist das Replizieren von flüchtigen erforderlich.
-   Quelle1 ist ein Quell Register. Bei der Auswahl einer einzelnen Komponente ist das Replizieren von flüchtigen erforderlich.

## <a name="remarks"></a>Bemerkungen

Diese Anweisung wird in den folgenden Versionen unterstützt.



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| \_Comp Abbrechen           |      |      |      |      |      | x    | x     | x    | x     |



 

Wenn der Vergleich true ist, wird er wie gezeigt aus der aktuellen Schleife unterbrochen.


```
if (!(src0 comparison src1))
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




