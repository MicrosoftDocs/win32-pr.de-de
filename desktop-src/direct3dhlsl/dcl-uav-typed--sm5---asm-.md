---
title: dcl_uav_typed (sm5 - asm)
description: Deklarieren Sie eine ungeordnete Zugriffsansicht (UAV) für die Verwendung durch einen Shader. | dcl_uav_typed (sm5 - asm)
ms.assetid: F9F5583F-E3D0-447F-9227-BBB1B4E71934
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ec321389f8c8296bda8ccd1eba947b5ba38adc80c94b3c8c0685b069fcdafbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950580"
---
# <a name="dcl_uav_typed-sm5---asm"></a>dcl \_ uav \_ typed (sm5 - asm)

Deklarieren Sie eine ungeordnete Zugriffsansicht (UAV) für die Verwendung durch einen Shader.



| dcl \_ uav \_ typed \[ \_ glc \] dstUAV, dimension, type |
|--------------------------------------------------|



 



| Element                                                                                           | BESCHREIBUNG                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[im \] UAV.<br/>                                                                        |
| <span id="dimension"></span><span id="DIMENSION"></span>*Dimension*<br/>                 | \[in \] Gibt an, wie viele Dimensionen die Anweisungen, die auf die UAV zugreifen, bereitstellen.<br/> |
| <span id="type"></span><span id="TYPE"></span>*Typ*<br/>                                | \[in \] Der Typ des UAV.<br/>                                                            |



 

## <a name="remarks"></a>Hinweise

*dstUAV ist* ein u-Register, das als Verweis auf eine UnorderedAccessView deklariert wird, die an den UAV-Slot in der \# API gebunden werden \# muss.

Die Dimension muss buffer, Texture1D, Texture1DArray, Texture2D, Texture2DArray oder Texture3D sein. Dies gibt an, wie viele Dimensionen anweisungen, die auf den UAV zugreifen, bereitstellen: 1 (Texture1D, Buffer), 2 (Texture1DArray, Texture2D) oder 3 (Texture2DArray, Texture3D).

Typ: {UNORM, SNORM, UINT, SINT, FLOAT}. Vorgänge, die mit dem deklarierten u durchgeführt werden, müssen mit dem hier deklarierten Typ kompatibel sein, und die an den Slot gebundene UAV muss \# \# ebenfalls denselben Typ haben.

Das \_ glc-Flag steht für "global zusammenhängende". Das Fehlen von glc bedeutet, dass die UAV im Compute-Shader nur als "gruppenreigent" oder bei einem Aufruf eines Einzelnen Pixel-Shaders \_ als "lokal zusammenhängend" deklariert wird.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Da UAVs in allen Shaderstufen für Direct3D 11.1 verfügbar sind, gilt diese Anweisung für alle Shaderstufen für die Direct3D 11.1-Runtime, die ab Windows 8.



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

> [!Note]  
> Diese Anweisung wird in Compute-Shader 4.x nicht unterstützt.

 

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

 

 





