---
title: dcl_tessellator_partitioning (sm5 - asm)
description: Deklarieren Sie die Mosaikpartitionierung in einem Deklarationsabschnitt für den Hüllen-Shader.
ms.assetid: 6EA00C6B-A0DE-4CE4-8B52-1337CA92CA5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae40873db4042e568ae637634e75db6f4746985a316bf9c1e092e6b0925b51b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068500"
---
# <a name="dcl_tessellator_partitioning-sm5---asm"></a>dcl \_ tessellator \_ partitioning (sm5 - asm)

Deklarieren Sie die Mosaikpartitionierung in einem Deklarationsabschnitt für den Hüllen-Shader.



| dcl \_ tessellator \_ partitioning {partitioning \_ integer\| Partitionierung \_ pow2\|Partitionierung \_ Bruch \_ ungerade\| Partitionierung \_ von Fractional \_ Even} |
|---------------------------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | BESCHREIBUNG                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*Partitionierung der \_ \| ganzzahligen \_ Partitionierung pow2 \| Partitionierung \_ fractional \_ odd \| partitioning \_ fractional \_ even*<br/> | \[in \] Die Mosaikpartitionierung.<br/> |



 

## <a name="remarks"></a>Hinweise

Aus Hardwaresicht verhält \_ sich pow2 wie eine ganze \_ Zahl. Es liegt in der Zuständigkeit des HLSL-Shaderautors und/oder Compilercodes, TessFactors auf 2-Werte zu runden.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf                 | Domain | Geometrie | Pixel | Compute |
|--------|----------------------|--------|----------|-------|---------|
|        | Abschnitt "Deklarationen" |        |          |       |         |



 

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

 

 





