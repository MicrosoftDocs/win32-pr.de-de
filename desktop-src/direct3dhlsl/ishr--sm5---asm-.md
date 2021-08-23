---
title: ishr (sm5 - asm)
description: Arithmetische Verschiebung nach rechts (Erweiterung des Vorzeichens). | ishr (sm5 - asm)
ms.assetid: 8124B6C3-4576-4616-85A9-A2DD19EB6BB9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c75d64ded9beb6cdc5660d6157b15fc989863ee9e907e67c00854fe7cfe161
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488330"
---
# <a name="ishr-sm5---asm"></a>ishr (sm5 - asm)

Arithmetische Verschiebung nach rechts (Erweiterung des Vorzeichens).



| ishl dest \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle\] |
|--------------------------------------------------------|



 



| Element                                                            | Beschreibung                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Enthält die Ergebnisse der Verschiebung.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Anzahl der zu verschiebenden Bits.<br/>       |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Die zu verschiebenden 32-Bit-Werte.<br/>        |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung führt eine komponentenweise arithmetische Verschiebung jedes 32-Bit-Werts in *src0* durch eine ganzzahlige Bitanzahl ohne Vorzeichen aus, die von den LSB 5 Bits (0-31 Bereich) in *src1* bereitgestellt wird, und repliziert den Wert von Bit 31. Das 32-Bit-Ergebnis pro Komponente wird in *dest platziert.*

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
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

 

 





