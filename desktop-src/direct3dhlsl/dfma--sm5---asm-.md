---
title: DFMA (SM5-ASM)
description: Führt ein Add-in mit einer Fused-Multiplikation aus
ms.assetid: 5BE96CDB-1756-4EBE-B4CC-69EFF098A4F1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e6cafc71dbc7d57655524b1b87c9c5b9ba20f3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313656"
---
# <a name="dfma-sm5---asm"></a>DFMA (SM5-ASM)

Führt ein Add-in mit einer Fused-Multiplikation aus



| DFMA \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle2 \[ \_ ABS \] \[ . Swizzle\] |
|----------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse des Vorgangs Ergebnisses. Der Ergebniswert muss auf 0,5 ULP genau sein.<br/> *dest*  =  *src0* \* *Quelle1*  +  *Quelle2*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] den Komponenten, die mit *Quelle1* multipliziert werden sollen.<br/>                                                                                                 |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[in \] den Komponenten, die mit *src0* multipliziert werden sollen.<br/>                                                                                                 |
| <span id="src2"></span><span id="SRC2"></span>*Quelle2*<br/> | \[in \] den Komponenten, die zu *src0* Quelle1 hinzugefügt werden sollen \* .<br/>                                                                                               |



 

## <a name="remarks"></a>Bemerkungen

Shader, die diese Anweisung verwenden, werden mit einem shaderflag gekennzeichnet, das dazu führt, dass Sie nicht gebunden werden, es sei denn, die folgenden Bedingungen sind erfüllt.

-   Das System unterstützt DirectX 11,1.
-   Das System enthält einen WDDM 1,2-Treiber.
-   Der Treiber meldet die Unterstützung für diese Anweisung über **D3D11 \_ Feature \_ Data \_ D3D11 \_ options. "Extendeddoublesshaderinstructions** " ist auf " **true**" festgelegt.

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

 

 





