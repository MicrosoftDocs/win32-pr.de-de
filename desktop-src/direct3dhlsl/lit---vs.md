---
title: Lit-vs
description: Bietet partielle Unterstützung für Beleuchtung durch Berechnen von Beleuchtungs Koeffizienten aus zwei Punkt Produkten und einem Exponenten.
ms.assetid: e0ed1a75-6682-4d05-b0e5-dc65e201de98
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99c25c377ff6064a704d56b9e7b31d41b37117e5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976393"
---
# <a name="lit---vs"></a>Lit-vs

Bietet partielle Unterstützung für Beleuchtung durch Berechnen von Beleuchtungs Koeffizienten aus zwei Punkt Produkten und einem Exponenten.

## <a name="syntax"></a>Syntax



| Lit DST, src |
|--------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| gezündet                    | x    | x    | x    | x     | x    | x     |



 

Es wird davon ausgegangen, dass der Quell Vektor die Werte enthält, die im folgenden Pseudocode angezeigt werden.


```
src.x = N*L        ; The dot product between normal and direction to light
src.y = N*H        ; The dot product between normal and half vector
src.z = ignored    ; This value is ignored
src.w = exponent   ; The value must be between -128.0 and 128.0
```



Das folgende Code Fragment zeigt die ausgeführten Vorgänge.


```
dest.x = 1;
dest.y = 0;
dest.z = 0;
dest.w = 1;

float power = src.w;
const float MAXPOWER = 127.9961f;
if (power < -MAXPOWER)
    power = -MAXPOWER;          // Fits into 8.8 fixed point format
else if (power > MAXPOWER)
    power = MAXPOWER;          // Fits into 8.8 fixed point format

if (src.x > 0)
{
    dest.y = src.x;
    if (src.y > 0)
    {
        // Allowed approximation is EXP(power * LOG(src.y))
        dest.z = (float)(pow(src.y, power));
    }
}
```



Die arithmetische Genauigkeit mit eingeschränkter Genauigkeit ist bei der Auswertung der y-Zielkomponente (dest. y) zulässig. Eine-Implementierung muss mindestens acht Bruch Bits im Power-Argument unterstützen. Punkt Produkte werden mit normalisierten Vektoren berechnet, und die Grenzwerte liegen zwischen-128 und 128.

Der Fehler sollte mit einer Kombination aus [LogP-vs](logp---vs.md) und [Exp-vs](exp---vs.md) oder nicht mehr als ungefähr einem signifikanten Bit für eine 8-Bit-Farbkomponente übereinstimmen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




