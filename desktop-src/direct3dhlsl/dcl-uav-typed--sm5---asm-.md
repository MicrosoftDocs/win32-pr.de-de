---
title: dcl_uav_typed (SM5-ASM)
description: Deklarieren Sie eine ungeordnete Zugriffs Ansicht (UAV) für die Verwendung durch einen Shader. | dcl_uav_typed (SM5-ASM)
ms.assetid: F9F5583F-E3D0-447F-9227-BBB1B4E71934
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b789714c7ec825620b73e387fa8a4dd73e1a590d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995745"
---
# <a name="dcl_uav_typed-sm5---asm"></a>DCL \_ -UAV- \_ typisiert (SM5-ASM)

Deklarieren Sie eine ungeordnete Zugriffs Ansicht (UAV) für die Verwendung durch einen Shader.



| DCL \_ UAV \_ typisiertes \[ \_ GLC \] dstuav, Dimension, Typ |
|--------------------------------------------------|



 



| Element                                                                                           | BESCHREIBUNG                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstuav*<br/> | \[in \] der UAV.<br/>                                                                        |
| <span id="dimension"></span><span id="DIMENSION"></span>*Maß*<br/>                 | \[in \] gibt an, wie viele Dimensionen die Anweisungen für den Zugriff auf die UAV bereitstellen.<br/> |
| <span id="type"></span><span id="TYPE"></span>*Sorte*<br/>                                | \[in \] der UAV-Art.<br/>                                                            |



 

## <a name="remarks"></a>Bemerkungen

*dstuav* wird \# als Verweis auf eine unorderedaccessview deklariert, die an den UAV-Slot \# an der API gebunden werden muss.

Die Dimension muss Buffer, Texture1D, Texture1DArray, Texture2D, Texture2DArray oder Texture3D lauten. Dies gibt an, wie viele Dimensionen alle Anweisungen, die auf die UAV zugreifen, bereitstellen: 1 (Texture1D, Buffer), 2 (Texture1DArray, Texture2D) oder 3 (Texture2DArray, Texture3D).

Typ: {unorm, snorm, uint, Sint, float}. Vorgänge, die mit der deklarierten u ausgeführt \# werden, müssen mit dem hier deklarierten Typ kompatibel sein, und die an Slot gebundene UAV \# muss ebenfalls denselben Typ aufweisen.

Das \_ GLC-Flag steht für "Global kohärent". Das Fehlen von \_ GLC bedeutet, dass die UAV im COMPUTE-Shader nur als "zusammenhängender Gruppe" oder "lokal kohärent" in einem einzelnen Pixelshader-Aufruf deklariert wird.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

> [!Note]  
> Diese Anweisung wird in Compute-Shader 4. x nicht unterstützt.

 

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

 

 





