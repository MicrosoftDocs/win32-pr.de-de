---
title: DMin (SM5-ASM)
description: Die minimale Genauigkeit für die Komponente mit doppelter Genauigkeit.
ms.assetid: 77331B4D-C4B5-49B2-BB6A-77BD5050B575
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e199b01c68acca6609123425438f309af872fb4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038338"
---
# <a name="dmin-sm5---asm"></a>DMin (SM5-ASM)

Die minimale Genauigkeit für die Komponente mit doppelter Genauigkeit.



| DMin \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle\] |
|---------------------------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                                                                                                                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse der Ergebnisse des Vorgangs.<br/> *dest*  =  *src0*  <  *Quelle1* ? *src0* : *Quelle1*<br/> < wird anstelle von <= verwendet, sodass, wenn min (x, y) = x, dann Max (x, y) = y ist. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] den Komponenten, die mit *Quelle1* verglichen werden sollen.<br/>                                                                                                                                                     |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[in \] den Komponenten, die mit *src0* verglichen werden sollen.<br/>                                                                                                                                                     |



 

## <a name="remarks"></a>Bemerkungen

Nan hat eine besondere Behandlung. Wenn ein Quell Operand NaN ist, wird der andere Quell Operand zurückgegeben. Die Auswahl erfolgt pro Komponente. Wenn beide Nan sind, wird eine Nan-Darstellung zurückgegeben.

Die gültigen Werte für die Quellparameter lauten ". xyzw", ". xyxy", ". zwxy", ". zwzw". Die gültigen *dest* -Masken sind. XY,. zw und. xyzw. Die folgenden *src* -Zuordnungen sind Post-Swizzle:

-   *dest* ist eine doppelte vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).
-   *src0* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).
-   *Quelle1* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).

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

 

 





