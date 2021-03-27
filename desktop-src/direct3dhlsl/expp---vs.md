---
title: EXPP-vs
description: Stellt eine exponentielle partielle Genauigkeit von 2X bereit.
ms.assetid: ac080ac9-5dfd-49e4-92ea-50bb26844ff6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0d57e2723c90eee8df728aa540baeab86932e773
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719404"
---
# <a name="expp---vs"></a>EXPP-vs

Stellt eine exponentielle partielle Genauigkeit 2<sup>x</sup>bereit.

## <a name="syntax"></a>Syntax



| EXPP DST, src. Stuben|Teenie|z|Löw |
|----------------------------|



 

Hierbei gilt:

-   DST ist das Ziel Register.
-   src ist ein Quell Register. Das Quell Register erfordert die explizite Verwendung von replizierten Strichen, d. h. genau einer der x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-äquivalente) muss angegeben werden.
-   {x \| y \| z \| w} ist das erforderliche Replizieren von replizieren für das Quell Register.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| EXPP                   | x    | x    | x    | x     | x    | x     |



 

### <a name="vs_1_1"></a>vs \_ 1 \_ 1

Die [Exp-vs-](exp---vs.md) Anweisung ist abhängig von den Scheitelpunkt-Shader-Versionen unterschiedlich.

In vs \_ 1 \_ 1 ergibt die EXPP-Anweisung die folgenden Ergebnisse:


```
v = the scalar value from the source register with a replicate swizzle

dest.x = pow(2, floor(v))
dest.y = v - floor(v)
dest.z = pow(2, v) (partial-precision)
dest.w = 1
```



In vs \_ 2 \_ 0 und aufwärts führt die EXPP-Anweisung die folgenden Ergebnisse aus:


```
v = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow(2, v) (partial-precision)
```



### <a name="vs_2_0"></a>vs \_ 2 \_ 0

In vs \_ 2 \_ 0 und oben funktioniert die-Anweisung wie folgt:


```
float V = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow( 2, V ) (partial-precision)
```



Die-Anweisung bietet mindestens 10 Bits an Genauigkeit.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




