---
title: sincos – ps
description: Berechnet Sinus und Kosinus im Bogenmaß. | sincos – ps
ms.assetid: 639237ea-1b7a-4959-9093-78f134c11863
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 95f61c3a1cfc15f699e0e637dce8d58b9517ffe58ef36e529ec297661bff6a3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671570"
---
# <a name="sincos---ps"></a>sincos – ps

Berechnet Sinus und Kosinus im Bogenmaß.

## <a name="syntax"></a>Syntax

### <a name="ps_2_0-and-ps_2_x"></a>ps \_ 2 \_ 0 und ps \_ 2 \_ x



| sincos dst. {x\|y\|xy}, src0. {x\|y\|z\|w}, src1, src2 |
|------------------------------------------------------|



 

Hierbei gilt:

-   dst ist das Zielregister und muss ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) sein. Das Zielregister muss genau eine der folgenden drei Masken aufweisen: .x \| .y \| .xy.
-   src0 ist ein Quellregister, das den Eingabewinkel bereitstellt, der innerhalb von \[ -pi, +pi sein \] muss. {x \| y \| z \| w} ist die erforderliche Replizieren-Swizzle.
-   src1 und src2 sind Quellregister und müssen zwei verschiedene [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c) \# sein. Die Werte von src1 und src2 müssen die Werte der Makros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) bzw. [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) sein.

### <a name="ps_3_0"></a>ps \_ 3 \_ 0



| sincos dst. {x\|y\|xy}, src0. {x\|y\|z\|w} |
|------------------------------------------|



 

Hierbei gilt:

-   dst ist ein Zielregister und muss ein [temporäres Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) sein. Das Zielregister muss genau eine der folgenden drei Masken aufweisen: .x \| .y \| .xy.
-   src0 ist ein Quellregister, das den Eingabewinkel bereitstellt, der innerhalb von \[ -pi, +pi sein \] muss. {x \| y \| z \| w} ist die erforderliche Replizieren-Swizzle.

## <a name="remarks"></a>Hinweise



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| sincos                |      |      |      |      | x    | x    | x     | x    | x     |



 

### <a name="ps_2_0-and-ps_2_x"></a>ps \_ 2 \_ 0 und ps \_ 2 \_ x

Für ps \_ 2 \_ 0 und ps \_ 2 \_ x können Sincos mit Prädikation verwendet werden, aber mit einer Einschränkung für die Swizzle des [Prädikatregisters](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0): Nur Replizieren von Swizzle (.x \| .y \| .z \| .w) ist zulässig.

Für ps \_ 2 \_ 0 und ps \_ 2 \_ x funktioniert die Anweisung wie folgt (V = der Skalarwert von src0 mit einer Replizieren-Swizzle):

-   Wenn die Schreibmaske .x ist:
    ```
    dest.x = cos(V)
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Wenn die Schreibmaske .y ist:
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Wenn die Schreibmaske .xy ist:
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="ps_3_0"></a>ps \_ 3 \_ 0

Für ps \_ 3 \_ 0 kann sincos ohne Einschränkung mit Prädikation verwendet werden. Weitere Informationen finden Sie unter [Prädikatregister.](dx9-graphics-reference-asm-ps-registers-predicate.md)

Für ps \_ 3 \_ 0 funktioniert die Anweisung wie folgt (V = der Skalarwert von src0 mit einem Replizieren von Swizzle):

-   Wenn die Schreibmaske .x ist:
    ```
    dest.x = cos(V)
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Wenn die Schreibmaske .y ist:
    ```
    dest.x is not touched by the instruction
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Wenn die Schreibmaske .xy ist:
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

Die Anwendung kann mithilfe des folgenden Shader-Pseudocodes einen beliebigen Winkel (im Bogenmaß) dem Bereich \[ "-pi" und "+pi" \] zuordnen:


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

 

 
