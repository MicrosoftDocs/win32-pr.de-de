---
title: SinCos-PS
description: Berechnet Sinus und Kosinus im Bogenmaße. | SinCos-PS
ms.assetid: 639237ea-1b7a-4959-9093-78f134c11863
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1e7ccdca91af206862384ae14cf25a85d0817814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995542"
---
# <a name="sincos---ps"></a>SinCos-PS

Berechnet Sinus und Kosinus im Bogenmaße.

## <a name="syntax"></a>Syntax

### <a name="ps_2_0-and-ps_2_x"></a>PS \_ 2 \_ 0 und PS \_ 2 \_ x



| SinCos DST. Stuben|Teenie|XY}, src0. Stuben|Teenie|z|w}, Quelle1, Quelle2 |
|------------------------------------------------------|



 

Hierbei gilt:

-   DST ist das Ziel Register und muss ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) sein. Das Ziel Register muss genau eine der folgenden drei Masken aufweisen:. x \| . y \| . XY.
-   src0 ist ein Quell Register, das den Eingabe Winkel bereitstellt, der innerhalb von \[ -Pi, + Pi liegen muss \] . {x \| y \| z \| w} ist das erforderliche Replizieren von replizieren.
-   Quelle1 und Quelle2 sind Quell Register und müssen zwei unterschiedliche [Konstante float-Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c \# ) aufweisen. Die Werte von Quelle1 und Quelle2 müssen der der Makros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) bzw. [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) sein.

### <a name="ps_3_0"></a>PS \_ 3 \_ 0



| SinCos DST. Stuben|Teenie|XY}, src0. Stuben|Teenie|z|Löw |
|------------------------------------------|



 

Hierbei gilt:

-   DST ist ein Ziel Register, das ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r) sein muss \# . Das Ziel Register muss genau eine der folgenden drei Masken aufweisen:. x \| . y \| . XY.
-   src0 ist ein Quell Register, das den Eingabe Winkel bereitstellt, der innerhalb von \[ -Pi, + Pi liegen muss \] . {x \| y \| z \| w} ist das erforderliche Replizieren von replizieren.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| SinCos                |      |      |      |      | x    | x    | x     | x    | x     |



 

### <a name="ps_2_0-and-ps_2_x"></a>PS \_ 2 \_ 0 und PS \_ 2 \_ x

Für PS \_ 2 \_ 0 und PS \_ 2 \_ x kann SinCos mit dem Prädikat verwendet werden, jedoch mit einer Einschränkung für das ausweichende des [Prädikats](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0): nur replizieren (. x \| . y \| . z \| . w) ist zulässig.

Für PS \_ 2 \_ 0 und PS \_ 2 \_ x funktioniert die-Anweisung wie folgt (V = der Skalarwert von src0 mit einem replizierten Swizzle):

-   Wenn die Schreib Maske den Wert. x hat:
    ```
    dest.x = cos(V)
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Wenn die Schreib Maske ". y" lautet:
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Wenn die Schreib Maske. XY lautet:
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="ps_3_0"></a>PS \_ 3 \_ 0

Für PS \_ 3 \_ 0 kann SinCos mit Prädikat ohne Einschränkung verwendet werden. Siehe [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).

Für PS \_ 3 \_ 0 funktioniert die-Anweisung wie folgt (V = der Skalarwert von src0 mit einem replizierten Swizzle):

-   Wenn die Schreib Maske den Wert. x hat:
    ```
    dest.x = cos(V)
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Wenn die Schreib Maske ". y" lautet:
    ```
    dest.x is not touched by the instruction
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Wenn die Schreib Maske. XY lautet:
    ```
    dest.x = cos(V)
    dest.y = sin(V)
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

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
