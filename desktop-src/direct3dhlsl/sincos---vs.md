---
title: SinCos-vs
description: Berechnet Sinus und Kosinus im Bogenmaße. | SinCos-vs
ms.assetid: 733a3980-ceaf-43dc-a862-923c369e4a65
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca70a319852346c6e75ba544489d033a861d4c3b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961484"
---
# <a name="sincos---vs"></a>SinCos-vs

Berechnet Sinus und Kosinus im Bogenmaße.

## <a name="syntax"></a>Syntax

### <a name="vs_2_0-and-vs_2_x"></a>vs \_ 2 \_ 0 und vs \_ 2 \_ x



| SinCos DST. Stuben|Teenie|XY}, src0. Stuben|Teenie|z|w}, Quelle1, Quelle2 |
|------------------------------------------------------|



 

Hierbei gilt:

-   DST ist das Ziel Register und muss ein [temporäres Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ) sein. Das Ziel Register muss genau eine der folgenden drei Masken aufweisen:. x \| . y \| . XY.
-   src0 ist ein Quell Register, das den Eingabe Winkel bereitstellt, der innerhalb von \[ -Pi, + Pi liegen muss \] . {x \| y \| z \| w} ist das erforderliche Replizieren von replizieren.
-   Quelle1 und Quelle2 sind Quell Register und müssen zwei unterschiedliche [Konstante float-Register](dx9-graphics-reference-asm-vs-registers-constant-float.md) (c \# ) aufweisen. Die Werte von Quelle1 und Quelle2 müssen der der Makros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) bzw. [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) sein.

### <a name="vs_3_0"></a>vs \_ 3 \_ 0



| SinCos DST. Stuben|Teenie|XY}, src0. Stuben|Teenie|z|Löw |
|------------------------------------------|



 

Hierbei gilt:

-   DST ist ein Ziel Register, das ein [temporäres Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r) sein muss \# . Das Ziel Register muss genau eine der folgenden drei Masken aufweisen:. x \| . y \| . XY.
-   src0 ist ein Quell Register, das den Eingabe Winkel bereitstellt, der innerhalb von \[ -Pi, + Pi liegen muss \] . {x \| y \| z \| w} ist das erforderliche Replizieren von replizieren.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| SinCos                 |      | x    | x    | x     | x    | x     |



 

### <a name="vs_2_0-and-vs_2_x-remarks"></a>\_ \_ Anmerkungen zu vs 2 0 und vs \_ 2 \_ x

Für vs \_ 2 \_ 0 und vs \_ 2 \_ x können SinCos mit Prädikaten verwendet werden, jedoch mit einer Einschränkung für das ausweichende des [Prädikats](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0): nur replizieren (. x \| . y \| . z \| . w) ist zulässig.

Für vs \_ 2 \_ 0 und vs \_ 2 \_ x verhält sich die-Anweisung wie folgt: (V = der skalare Wert von src0 mit einem replizierten Swizzle):

-   Wenn die Schreib Maske den Wert. x hat:
    ```
    dest.x = cos( V )
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Wenn die Schreib Maske ". y" lautet:
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Wenn die Schreib Maske. XY lautet:
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="vs_3_0-remarks"></a>vs \_ 3 \_ 0-Hinweise

Für vs \_ 3 \_ 0 kann SinCos mit einem Prädikat ohne Einschränkung verwendet werden. Siehe [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).

Für vs \_ 3 \_ 0 funktioniert die-Anweisung wie folgt: (V = der Skalarwert von src0 mit einem replizierten Swizzle)

-   Wenn die Schreib Maske den Wert. x hat:
    ```
    dest.x = cos( V )
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Wenn die Schreib Maske ". y" lautet:
    ```
    dest.x is not touched by the instruction
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Wenn die Schreib Maske. XY lautet:
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

Die Anwendung kann \[ \] mit dem folgenden shaderpseudocode einen beliebigen Winkel (im Bogenmaße) zum Range-Pi und PI zuordnen:


```
def c0, pi, 0.5, 2*pi, 1/(2*pi)
mad r0.x, input_angle, c0.w, c0.y
frc r0.x, r0.x
mad r0.x, r0.x, c0.z, -c0.x
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
