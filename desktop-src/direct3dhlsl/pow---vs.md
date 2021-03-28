---
title: Pow-vs
description: Abs (src0) mit vollständiger Genauigkeit Quelle1. | Pow-vs
ms.assetid: 51da86c6-bafa-42e0-90a5-d1545e39e600
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3263fa19015bc32c94ae714891c3bbb2128c9463
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219174"
---
# <a name="pow---vs"></a>Pow-vs

Abs (src0) mit vollständiger Genauigkeit<sup>Quelle1</sup>.

## <a name="syntax"></a>Syntax



| Pow DST, src0, Quelle1 |
|---------------------|



 

where

-   DST ist das Ziel Register.
-   src0 ist ein Eingabe Quellen Register. Das Quell Register erfordert die explizite Verwendung von replizierten Strichen, d. h. genau einer der x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-äquivalente) muss angegeben werden.
-   Quelle1 ist ein Eingabe Quellen Register. Das Quell Register erfordert die explizite Verwendung von replizierten Strichen, d. h. genau einer der x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-äquivalente) muss angegeben werden.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| pow                    |      | x    | x    | x     | x    | x     |



 

Diese Anweisung funktioniert wie hier gezeigt.


```
dest = pow(abs(src0), src1);
```



Dabei handelt es sich um eine skalare Anweisung. Daher sollten die Quell Register über repliziert werden, um anzugeben, welche Kanäle verwendet werden.

Das skalare Ergebnis wird in alle vier Ausgabekanäle repliziert.

Diese Anweisung kann als Exp (Quelle1 \* Log (src0)) erweitert werden.

Die Genauigkeit ist nicht kleiner als 15 Bits.

Das dest-Register muss ein temporäres Register sein und sollte nicht dasselbe Register wie Quelle1 sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




