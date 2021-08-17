---
title: lit – vs
description: Bietet teilweise Unterstützung für die Beleuchtung, indem Die Lichtkoeffizienten aus zwei Punktprodukten und einem Exponenten berechnet werden.
ms.assetid: e0ed1a75-6682-4d05-b0e5-dc65e201de98
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3e5b5ff3451424251d778886af3841c673ce5a85d91022db9144c62574c16640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118089323"
---
# <a name="lit---vs"></a>lit – vs

Bietet teilweise Unterstützung für die Beleuchtung, indem Die Lichtkoeffizienten aus zwei Punktprodukten und einem Exponenten berechnet werden.

## <a name="syntax"></a>Syntax



| lit dst, src |
|--------------|



 

where

-   dst ist das Zielregister.
-   src ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Beleuchtet                    | x    | x    | x    | x     | x    | x     |



 

Es wird davon ausgegangen, dass der Quellvektor die im folgenden Pseudocode gezeigten Werte enthält.


```
src.x = N*L        ; The dot product between normal and direction to light
src.y = N*H        ; The dot product between normal and half vector
src.z = ignored    ; This value is ignored
src.w = exponent   ; The value must be between -128.0 and 128.0
```



Das folgende Codefragment zeigt die ausgeführten Vorgänge.


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



Arithmetik mit geringerer Genauigkeit ist bei der Auswertung der Zielkomponente y (dest.y) akzeptabel. Eine Implementierung muss mindestens acht Bruchbits im Potenzargument unterstützen. Punktprodukte werden mit normalisierten Vektoren berechnet, und die Klammergrenzwerte liegen zwischen -128 und 128.

Der Fehler sollte einer [Logp-/ vs.](logp---vs.md) [exp- vs-Kombination](exp---vs.md) oder nicht mehr als einem signifikanten Bit für eine 8-Bit-Farbkomponente entsprechen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




