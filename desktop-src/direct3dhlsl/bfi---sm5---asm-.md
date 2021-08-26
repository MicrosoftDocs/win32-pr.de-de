---
title: bfi (sm5 - asm)
description: Platzieren Sie bei einem Bitbereich von der LSB einer Zahl diese Anzahl von Bits in einer anderen Zahl an einem beliebigen Offset.
ms.assetid: BA84C882-A141-4AD2-8FD9-C60F1483FC65
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1452b1f15525753738ee6f74a1bd43473f43033346c9b493cd72222eaab22cb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068530"
---
# <a name="bfi-sm5---asm"></a>bfi (sm5 - asm)

Platzieren Sie bei einem Bitbereich von der LSB einer Zahl diese Anzahl von Bits in einer anderen Zahl an einem beliebigen Offset.



| bfi dest \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle \] , src2 \[ .swizzle \] , src3 \[ .swizzle\] |
|-------------------------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse der Ergebnisse.<br/>                       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Bitfeldbreite, die von *src2 zu übernehmen ist.*<br/>           |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Der Bitfeldoffset zum Ersetzen von Bits in *src3*.<br/> |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[in \] Die Zahl, aus der die Bits entfernt werden. <br/>              |
| <span id="src3"></span><span id="SRC3"></span>*src3*<br/> | \[in \] Die Zahl mit bits, die ersetzt werden sollen.<br/>              |



 

## <a name="remarks"></a>Hinweise

Die LSB 5 Bits *von src0* stellen die Bitfeldbreite (0-31) für *src2 zur Verfügung.*

Die LSB 5 Bits von *src1* stellen den Bitfeldoffset (0-31) zur Verfügung, um mit dem Ersetzen von Bits in der aus *src3* gelesenen Zahl zu beginnen.

``` syntax
Given width, offset:
                bitmask = (((1 << width)-1) << offset) & 0xffffffff
                dest = ((src2 << offset) & bitmask) | (src3 & ~bitmask)
```

Diese Anweisung wird zum Packen von ganzen Zahlen oder Flags verwendet.

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

 

 





