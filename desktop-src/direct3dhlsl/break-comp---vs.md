---
title: break_comp vs
description: Unterbrechen Sie die aktuelle Schleife bedingt bei den nächstgelegenen endschleifen-vs oder ENDREP-vs.
ms.assetid: 01745e03-874a-4594-b6ab-12db22d0cb4a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 631998aeba6612d945495d8115a74d00f7e657c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857779"
---
# <a name="break_comp---vs"></a>" \_ Comp-vs" Abbrechen

Unterbrechen Sie die aktuelle Schleife bedingt bei den nächstgelegenen [endschleifen-vs](endloop---vs.md) oder [ENDREP-vs](endrep---vs.md).

## <a name="syntax"></a>Syntax



| Break \_ Comp src0, Quelle1 |
|------------------------|



 

Hierbei gilt:

-   \_comp ist ein Vergleich zwischen den beiden Quell Registern. Folgende Werte sind möglich: 

    | Syntax | Vergleich            |
    |--------|-----------------------|
    | \_siegt   | Größer als          |
    | \_General   | Kleiner als             |
    | \_Färbung   | Größer als oder gleich |
    | \_Kirchturm   | Kleiner als oder gleich    |
    | \_stecken   | Gleich              |
    | \_NES   | Ungleich          |

    

     

-   src0 ist ein Quell Register. Das Replizieren der Replizierung ist erforderlich, um eine einzelne Komponente auszuwählen.
-   Quelle1 ist ein Quell Register. Das Replizieren der Replizierung ist erforderlich, um eine einzelne Komponente auszuwählen.

## <a name="remarks"></a>Bemerkungen

Diese Anweisung wird in den folgenden Versionen unterstützt.



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| \_Comp Abbrechen            |      |      | x    | x     | x    | x     |



 

Wenn der Vergleich true ist, wird er wie gezeigt aus der aktuellen Schleife unterbrochen.


```
if (src0 comparison src1)
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




