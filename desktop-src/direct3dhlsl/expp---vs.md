---
title: expp im Vergleich zu
description: Stellt eine 2x-Teilgenauigkeit mit exponentieller Genauigkeit zur
ms.assetid: ac080ac9-5dfd-49e4-92ea-50bb26844ff6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e8717edc045f50cc572d675dbec405b01fda49503349e9716210dfcae23fb277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982450"
---
# <a name="expp---vs"></a>expp im Vergleich zu

Stellt eine partielle Genauigkeit von exponentiell 2<sup>x zur</sup>

## <a name="syntax"></a>Syntax



| expp dst, src. {x\|y\|z\|w} |
|----------------------------|



 

Hierbei gilt:

-   dst ist das Zielregister.
-   src ist ein Quellregister. Das Quellregister erfordert die explizite Verwendung von "replicate swizzle", d.h. genau eine der .x-, .y-, .z-, .w swizzle-Komponenten (oder die Entsprechungen .r, .g, .b, .a) muss angegeben werden.
-   {x \| y \| z \| w} ist die erforderliche Replikation von Swizzle im Quellregister.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| expp                   | x    | x    | x    | x     | x    | x     |



 

### <a name="vs_1_1"></a>vs \_ 1 \_ 1

Die [Anweisung exp - vs](exp---vs.md) funktioniert je nach Vertex-Shaderversion unterschiedlich.

Im Vergleich \_ zu \_ 1 1 liefert die expp-Anweisung die folgenden Ergebnisse:


```
v = the scalar value from the source register with a replicate swizzle

dest.x = pow(2, floor(v))
dest.y = v - floor(v)
dest.z = pow(2, v) (partial-precision)
dest.w = 1
```



In vs \_ 2 \_ 0 und up gibt die expp-Anweisung die folgenden Ergebnisse aus:


```
v = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow(2, v) (partial-precision)
```



### <a name="vs_2_0"></a>vs \_ 2 \_ 0

In vs \_ 2 \_ 0 und up funktioniert die Anweisung wie die folgenden:


```
float V = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow( 2, V ) (partial-precision)
```



Die -Anweisung stellt mindestens 10 Bits Genauigkeit zur Verfügung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Anweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




