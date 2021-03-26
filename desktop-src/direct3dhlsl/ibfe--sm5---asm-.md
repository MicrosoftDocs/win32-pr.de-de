---
title: ibfe (SM5-ASM)
description: Wenn ein Bereich von Bits in einer Zahl angegeben ist, verschieben Sie diese Bits in den LSB und Signieren den MSB des Bereichs.
ms.assetid: 1ED39812-A89F-4325-82A0-DA2CCC55A99A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 805d5c1137e25d8b8fa560588b9e876ccc5c8748
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719368"
---
# <a name="ibfe-sm5---asm"></a>ibfe (SM5-ASM)

Wenn ein Bereich von Bits in einer Zahl angegeben ist, verschieben Sie diese Bits in den LSB und Signieren den MSB des Bereichs.



| ibfe dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle \] , Quelle2 \[ . Swizzle\] |
|--------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse der Ergebnisse des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] der Bitfeld Breite.<br/>                          |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[im \] Bitfeld-Offset.<br/>                         |
| <span id="src2"></span><span id="SRC2"></span>*Quelle2*<br/> | \[im \] zu Verschiebe Wert.<br/>                          |



 

## <a name="remarks"></a>Bemerkungen

In den lsb 5 Bits von src0 wird die Bitfeld Breite (0-31) bereitgestellt.

Mit den lsb 5 Bits von Quelle1 wird der Bitfeld-Offset (0-31) bereitgestellt.

Das folgende Beispiel zeigt die Verwendung dieser Anweisung.

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

 

 





