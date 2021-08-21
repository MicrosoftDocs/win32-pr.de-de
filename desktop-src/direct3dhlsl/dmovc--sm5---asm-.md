---
title: dmovc (sm5 - asm)
description: Komponentenweises bedingtes Verschieben. | dmovc (sm5 - asm)
ms.assetid: E376FE08-E251-4BE5-9F15-99B3B67A29C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc0ed15d81a91d8a93ce99eda3fa17b91900e0045301f1c5b5d1f56e4448954a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792381"
---
# <a name="dmovc-sm5---asm"></a>dmovc (sm5 - asm)

Komponentenweises bedingtes Verschieben.



| dmovc \[ \_ sat \] dest \[ .mask \] , src0 \[ .swizzle \] , \[ - \] src1 abs \[ \_ \] \[ .swizzle , \] \[ - \] src2 abs \[ \_ \] \[ .swizzle \] , |
|-----------------------------------------------------------------------------------------------------------------|



 



| Element                                                            | Beschreibung                                                                                              |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Das Move-Ziel.<br/> Wenn *src0*, dann *dest*  =  *src1* else *dest*  =  *src2*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponenten, für die die Bedingung zu testen ist.<br/>                                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Die zu verschiebenden Komponenten, wenn die Bedingung erfüllt ist.<br/>                                       |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[in \] Die zu verschiebenden Komponenten, wenn die Bedingung FALSE ist.<br/>                                      |



 

## <a name="remarks"></a>Hinweise

Im folgenden Beispiel wird die Verwendung dieser Anweisung veranschaulicht.

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

Die gültigen Masken für dest sind .xy, .zw, .xyzw.

Die gültigen Swizzles *für src0* sind alles. Die ersten beiden Komponenten nach dem Swizzle werden verwendet, um zwei 32-Bit-Bedingungswerte eingerückt zu werden.

Die gültigen Swizzles für *src1* und *src2,* die doubles enthalten, sind .xyzw, .xyxy, .zwxy, .zwzw. sind .xy, .zw und .xyzw.

Die folgenden *src-Zuordnungen* sind post swizzle:

-   *dest* ist ein double vec2 über (x 32LSB, y 32MSB) und (z 32LSB, w 32MSB).
-   *src0 ist* ein 32-Bit-/Komponenten-Vec2 über x und y (zw ignoriert).
-   *src1* ist ein double-vec2 zwischen (x 32LSB, y 32MSB) und (z 32LSB, w 32MSB).
-   *src2 ist* ein double-vec2 zwischen (x 32LSB, y 32MSB) und (z 32LSB, w 32MSB).

Bei den *Modifizierern für src1* und *src2*(mit Anderen als Swizzle) wird davon ausgegangen, dass die Daten doppelt sind. Das Fehlen von Modifizierern verschiebt Daten, ohne Bits zu ändern.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





