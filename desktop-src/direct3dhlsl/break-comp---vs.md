---
title: break_comp – vs
description: Bedingtes Ausbrechen der aktuellen Schleife beim nächsten Endloop – vs. oder endrep – vs.
ms.assetid: 01745e03-874a-4594-b6ab-12db22d0cb4a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a02bf34844918255086b318d9a13feeabbd6e75bdecca03684adaba70b420626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626560"
---
# <a name="break_comp---vs"></a>break \_ comp – vs

Bedingtes Ausbrechen der aktuellen Schleife beim nächsten [Endloop – vs.](endloop---vs.md) oder [endrep – im Vergleich zu](endrep---vs.md).

## <a name="syntax"></a>Syntax



| break \_ comp src0, src1 |
|------------------------|



 

Hierbei gilt:

-   \_comp ist ein Vergleich zwischen den beiden Quellregistern. Folgende Werte sind möglich: 

    | Syntax | Vergleich            |
    |--------|-----------------------|
    | \_Gt   | Größer als          |
    | \_Lt   | Kleiner als             |
    | \_Ge   | Größer als oder gleich |
    | \_Le   | Kleiner oder gleich    |
    | \_Eq   | Gleich              |
    | \_Ne   | Ungleich          |

    

     

-   src0 ist ein Quellregister. Replizieren von Swizzle ist erforderlich, um eine einzelne Komponente auszuwählen.
-   src1 ist ein Quellregister. Replizieren von Swizzle ist erforderlich, um eine einzelne Komponente auszuwählen.

## <a name="remarks"></a>Hinweise

Diese Anweisung wird in den folgenden Versionen unterstützt.



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| break \_ comp            |      |      | x    | x     | x    | x     |



 

Wenn der Vergleich true ist, wird er wie gezeigt aus der aktuellen Schleife herausbricht.


```
if (src0 comparison src1)
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Anweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




