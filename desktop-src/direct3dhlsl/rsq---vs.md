---
title: RSQ-vs
description: Berechnet die gegenseitige Quadratwurzel (nur positiv) des Quell Skalars. | RSQ-vs
ms.assetid: 1ac37dad-0cea-41af-8dae-f299896462b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f477d6f7d8a7ff94472c689bf5844183e2f016ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981800"
---
# <a name="rsq---vs"></a>RSQ-vs

Berechnet die gegenseitige Quadratwurzel (nur positiv) des Quell Skalars.

## <a name="syntax"></a>Syntax



| RSQ DST, src |
|--------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register. Das Quell Register erfordert die explizite Verwendung von replizierten Strichen, d. h. genau einer der x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-äquivalente) muss angegeben werden.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| RSQ                    | x    | x    | x    | x     | x    | x     |



 

Das folgende Code Fragment zeigt die ausgeführten Vorgänge.


```
float f = abs(src0);
if (f == 0)
    f = FLT_MAX
else
{
    if (f != 1.0)
        f = 1.0/(float)sqrt(f);
}

dest.z = dest.y = dest.z = dest.w = f;
```



Der absolute Wert wird vor der Verarbeitung übernommen.

Die Genauigkeit muss mindestens 1.0/(2 ² ²) absolute Fehler im Bereich (1,0, 4,0) betragen, da allgemeine Implementierungen die Mantisse und den Exponenten voneinander trennen.

Wenn die Quelle keine Indizes aufweist, wird die x-Komponente verwendet. Die Ausgabe muss genau 1,0 sein, wenn die Eingabe genau 1,0 ist. Eine Quelle von 0,0 ergibt unendlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




