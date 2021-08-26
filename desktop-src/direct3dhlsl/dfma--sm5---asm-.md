---
title: dfma (sm5 – asm)
description: Führt ein Fused-Multiply-Add aus.
ms.assetid: 5BE96CDB-1756-4EBE-B4CC-69EFF098A4F1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84952ed594ba8541223df072fa59550aded581e5517dee3d6f4168b7661a87aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068390"
---
# <a name="dfma-sm5---asm"></a>dfma (sm5 – asm)

Führt ein Fused-Multiply-Add aus.



| dfma \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , \[ - \] src1 abs \[ \_ \] \[ .swizzle , \] \[ - \] src2 abs \[ \_ \] \[ .swizzle\] |
|----------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse des Ergebnisses des Vorgangs. Der Ergebniswert muss auf 0,5 ULP genau sein.<br/> *dest*  =  *src0* \* *src1*  +  *src2*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponenten, die mit *src1* multipliziert werden sollen.<br/>                                                                                                 |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Die Komponenten, die mit *src0* multipliziert werden sollen.<br/>                                                                                                 |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[in \] Die Komponenten, die *src0* \* *src1* hinzugefügt werden sollen.<br/>                                                                                               |



 

## <a name="remarks"></a>Hinweise

Shader, die diese Anweisung verwenden, werden mit einem Shaderflag gekennzeichnet, das dazu führt, dass sie nicht gebunden werden, es sei denn, alle folgenden Bedingungen sind erfüllt.

-   Das System unterstützt DirectX 11.1.
-   Das System enthält einen WDDM 1.2-Treiber.
-   Der Treiber meldet Unterstützung für diese Anweisung über **D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS. ExtendedDoublesShaderInstructions** ist auf **TRUE** festgelegt.

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

 

 





