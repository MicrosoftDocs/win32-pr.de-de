---
title: ubfe (sm5 – asm)
description: Verschieben Sie bei einem Bereich von Bits in einer Zahl diese Bits auf den LSB, und legen Sie die verbleibenden Bits auf 0 fest.
ms.assetid: CC6BE378-2726-47A2-8E23-B8151521F72D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3149173bf495957bb38800234e4d853d0e32797254eecfdb3e5b77faf4498ac2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117722161"
---
# <a name="ubfe-sm5---asm"></a>ubfe (sm5 – asm)

Verschieben Sie bei einem Bereich von Bits in einer Zahl diese Bits auf den LSB, und legen Sie die verbleibenden Bits auf 0 fest.



| ubfe dest \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle \] , src2 \[ .swizzle\] |
|--------------------------------------------------------------------------|



 



| Element                                                            | Beschreibung                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Enthält die Ergebnisse der Anweisung.<br/>                     |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die LSB-5-Bits stellen die Bitfeldbreite (0-31) bereit.<br/>            |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Die LSB 5 Bits von *src1* stellen den Bitfeldoffset (0-31) bereit.<br/> |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[in \] Die zu verschiebende Zahl.<br/>                                         |



 

## <a name="remarks"></a>Hinweise

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

Verwenden Sie diese Anweisung, um ganze Zahlen oder Flags ohne Vorzeichen zu entpacken.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

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

[Shadermodell 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





