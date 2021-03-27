---
title: ubfe (SM5-ASM)
description: Wenn ein Bereich von Bits in einer Zahl angegeben ist, verschieben Sie diese Bits in den LSB, und legen Sie verbleibende Bits auf 0 fest.
ms.assetid: CC6BE378-2726-47A2-8E23-B8151521F72D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ebbe853ec1b53b452f32d79c9c2ec120e826b8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857771"
---
# <a name="ubfe-sm5---asm"></a>ubfe (SM5-ASM)

Wenn ein Bereich von Bits in einer Zahl angegeben ist, verschieben Sie diese Bits in den LSB, und legen Sie verbleibende Bits auf 0 fest.



| ubfe dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle \] , Quelle2 \[ . Swizzle\] |
|--------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] enthält die Ergebnisse der-Anweisung.<br/>                     |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[Geben Sie in \] den lsb 5 Bits die Bitfeld-Breite (0-31) an.<br/>            |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[Geben Sie in \] den lsb 5-Bits von *Quelle1* den Bitfeld-Offset (0-31) an.<br/> |
| <span id="src2"></span><span id="SRC2"></span>*Quelle2*<br/> | \[in \] der zu Verschiebe Zahl.<br/>                                         |



 

## <a name="remarks"></a>Bemerkungen

``` syntax
 
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ushr dest, dest, 32-width
                }
                else
                {
                    ushr dest, src2, offset
                }
```

Verwenden Sie diese Anweisung, um Ganzzahlen ohne Vorzeichen oder Flags zu entpacken.

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

 

 





