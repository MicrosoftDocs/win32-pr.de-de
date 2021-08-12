---
title: countbits (sm5 - asm)
description: Zählt die Anzahl der Bits, die in einer Zahl festgelegt sind.
ms.assetid: ED75487F-46FF-45F5-BEAA-7A32BEFB0571
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b13be61d470f5a8504c893f85bea4b7f500591d35118aec2bf6576b897a4b5d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286952"
---
# <a name="countbits-sm5---asm"></a>countbits (sm5 - asm)

Zählt die Anzahl der Bits, die in einer Zahl festgelegt sind.



| countbits dest \[ .mask \] , src0 \[ .swizzle\] |
|-------------------------------------------|



 



| Element                                                            | Beschreibung                                   |
|-----------------------------------------------------------------|-----------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse der Ergebnisse.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die 32-Bit-Eingabenummer.<br/>    |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung kann verwendet werden, um den Prozentsatz der Shadereingabeabdeckung zu berechnen.

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

 

 





