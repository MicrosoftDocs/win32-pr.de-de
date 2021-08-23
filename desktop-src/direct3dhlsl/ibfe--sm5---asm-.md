---
title: ibfe (sm5 - asm)
description: Wenn ein Bereich von Bits in einer Zahl angegeben ist, verschieben Sie diese Bits in die LSB und erweitern den MSB des Bereichs.
ms.assetid: 1ED39812-A89F-4325-82A0-DA2CCC55A99A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b04bfcaea154a8a63e9b118da12a8994398357b7c6a022a4589353c6c06eb34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949620"
---
# <a name="ibfe-sm5---asm"></a>ibfe (sm5 - asm)

Wenn ein Bereich von Bits in einer Zahl angegeben ist, verschieben Sie diese Bits in die LSB und erweitern den MSB des Bereichs.



| ibfe dest \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle \] , src2 \[ .swizzle\] |
|--------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse der Ergebnisse des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Bitfeldbreite.<br/>                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Der Bitfeldoffset.<br/>                         |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[in \] Der zu verschiebende Wert.<br/>                          |



 

## <a name="remarks"></a>Hinweise

Die LSB 5 Bits von src0 stellen die Bitfeldbreite (0-31) zur Verfügung.

Die LSB 5 Bits von src1 stellen den Bitfeldoffset (0-31) zur Verfügung.

Im folgenden Beispiel wird die Verwendung dieser Anweisung veranschaulicht.

``` syntax
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ishr dest, dest, 32-width
                }
                else
                {
                    ishr dest, src2, offset
                }
```

Verwenden Sie diese Anweisung, um ganze Zahlen oder Flags mit Vorzeichen zu entpacken.

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

 

 





