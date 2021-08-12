---
title: ushr (sm5 - asm)
description: Nach rechts verschieben. | ushr (sm5 - asm)
ms.assetid: C695CB6C-A6C9-4DC8-8EBE-70A0CFFC4981
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b4f0cacaa785b34eb8910f12ecfe3578bd47781e41110adc71f4a7a7d52858a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118283046"
---
# <a name="ushr-sm5---asm"></a>ushr (sm5 - asm)

Nach rechts verschieben.



| ubfe dest \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle\] |
|--------------------------------------------------------|



 



| Element                                                            | Beschreibung                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Enthält die Ergebnisse der Anweisung.<br/>                   |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die zu verschiebenden 32-Bit-Werte.<br/>                                |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[geben \] in LSB 5 Bits die Anzahl der zu verschiebenden Bits an (0-31).<br/> |



 

Diese Anweisung führt eine komponentenweise Verschiebung jedes 32-Bit-Werts in *src0* durch eine ganzzahlige Bitanzahl ohne Vorzeichen aus, die vom LSB 5 Bits (Bereich 0-31) in *src1* bereitgestellt wird, und fügt 0 ein. Die 32-Bit-Ergebnisse pro Komponente werden in *dest platziert.*

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

 

 





