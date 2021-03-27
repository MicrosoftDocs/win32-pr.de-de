---
title: dmuvc (SM5-ASM)
description: Bedingter Wechsel in Komponenten. | dmuvc (SM5-ASM)
ms.assetid: E376FE08-E251-4BE5-9F15-99B3B67A29C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e364e6340733c42ae69412db726851329eb2809d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104393930"
---
# <a name="dmovc-sm5---asm"></a>dmuvc (SM5-ASM)

Bedingter Wechsel in Komponenten.



| dmuvc \[ \_ Sat \] dest \[ . mask \] , src0 \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle2 \[ \_ ABS \] \[ . Swizzle \] , |
|-----------------------------------------------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                                              |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[im Verschiebungs \] Ziel.<br/> Wenn *src0*, dann *dest*  =  *Quelle1* Else *dest*  =  *Quelle2*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] den Komponenten, mit denen die Bedingung getestet werden soll.<br/>                                          |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[in \] den Komponenten, die verschoben werden sollen, wenn die Bedingung erfüllt ist.<br/>                                       |
| <span id="src2"></span><span id="SRC2"></span>*Quelle2*<br/> | \[in \] den zu Verschieb-Komponenten, wenn die Bedingung false ist.<br/>                                      |



 

## <a name="remarks"></a>Bemerkungen

Das folgende Beispiel zeigt die Verwendung dieser Anweisung.

``` syntax
                if(the dest mask contains .xy)
                {
                    if(the first 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the first double from src1 (post swizzle)
                        into dest.xy
                    }
                    else
                    {
                        copy the first double from src2 (post swizzle)
                        into dest.xy
                    }
                }
                if(the dest mask contains .zw)
                {
                    if(the second 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the second double from src1 (post swizzle)
                        into dest.zw
                    }
                    else
                    {
                        copy the second double from src2 (post swizzle)
                        into dest.zw
                    }
                }
```

Gültige Masken für dest sind. XY,. ZW,. xyzw.

Die gültigen Streifen für *src0* sind alles. Die ersten beiden Komponenten nach dem wischen werden verwendet, um die 2 32-Bit-Bedingungs Werte zu kennzeichnen.

Die gültigen Streifen für *Quelle1* und *Quelle2* , die doppelte enthalten, sind. xyzw,. xyxy,. zwxy,. zwzw. sind ". XY", ". zw" und ". xyzw".

Die folgenden *src* -Zuordnungen finden Sie nachfolgend:

-   *dest* ist eine doppelte vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).
-   *src0* ist ein 32-Bit-/Komponenten-vec2 über x und y hinweg (ZW wird ignoriert).
-   *Quelle1* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).
-   *Quelle2* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).

Bei den Modifizierern auf *Quelle1* und *Quelle2*, mit Ausnahme von Swizzle, wird davon ausgegangen, dass die Daten doppelt sind. Das Fehlen von Modifizierern verschiebt Daten, ohne Bits zu ändern.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Anweisung wird in den folgenden shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





