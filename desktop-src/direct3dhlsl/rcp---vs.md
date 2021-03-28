---
title: RCP-vs
description: Berechnet die gegenseitige des Quell Skalars. | RCP-vs
ms.assetid: be638a42-b693-461d-ab0a-3a6c0fa1acfc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 145a998cbca9dc3721d9c7d6ba251d539286a3f1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982011"
---
# <a name="rcp---vs"></a>RCP-vs

Berechnet die gegenseitige des Quell Skalars.

## <a name="syntax"></a>Syntax



| RCP DST, src |
|--------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register. Das Quell Register erfordert die explizite Verwendung von replizierten Strichen, d. h. genau einer der x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-äquivalente) muss angegeben werden.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| rcp                    | x    | x    | x    | x     | x    | x     |



 

Das folgende Code Fragment zeigt die ausgeführten Vorgänge.


```
float f = src0;
if(f == 0.0f)
{
    f = FLT_MAX;
}
else 
{
    if(f != 1.0)
    {
        f = 1/f;
    }
}

dest = f;
```



Die Ausgabe muss genau 1,0 sein, wenn die Eingabe genau 1,0 ist. Eine Quelle von 0,0 ergibt unendlich.

Die Genauigkeit muss mindestens 1.0/(2 ² ²) absolute Fehler im Bereich (1,0, 2,0) betragen, da allgemeine Implementierungen die Mantisse und den Exponenten voneinander trennen.

Wenn die Quelle keine Indizes aufweist, wird die x-Komponente verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




