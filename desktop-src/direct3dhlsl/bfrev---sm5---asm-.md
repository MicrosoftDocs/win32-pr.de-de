---
title: bfrev (sm5 - asm)
description: Umkehren einer 32-Bit-Zahl.
ms.assetid: 24F8209A-093E-4737-BF50-12F228024E9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87263a4ab2a4db54c25944905c36d81a4773e2f4eec40336b35fda03111dc3dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983540"
---
# <a name="bfrev-sm5---asm"></a>bfrev (sm5 - asm)

Umkehren einer 32-Bit-Zahl.



| bfrev dest \[ .mask \] , src0 \[ .swizzle\] |
|---------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse für *src0 mit* umgekehrten Bits.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die 32-Bit-Zahl, die umgekehrt werden soll.<br/>              |



 

## <a name="remarks"></a>Hinweise

Wenn sie beispielsweise 0x12345678, wird das Ergebnis 0x1e6a2c48.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





