---
title: dcl_tessellator_partitioning (SM5-ASM)
description: Deklarieren Sie die Mosaik-Partitionierung in einem Hull-Shader-Deklarations Abschnitt.
ms.assetid: 6EA00C6B-A0DE-4CE4-8B52-1337CA92CA5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6f6091301f95dd2364debec2bf54c0966c0e64
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389590"
---
# <a name="dcl_tessellator_partitioning-sm5---asm"></a>DCL \_ \_ -Mosaik-Partitionierung (SM5-ASM)

Deklarieren Sie die Mosaik-Partitionierung in einem Hull-Shader-Deklarations Abschnitt.



| DCL-Mosaik \_ Prozess- \_ Partitionierung {Partitionierungs \_ Ganzzahl \| Partitionierung \_ pow2 \|Partitionierung von \_ Bruchteil/ \_ ungeraden \| Partitionierung von \_ Bruchteilen \_ sogar} |
|---------------------------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | BESCHREIBUNG                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*Partitionierung von \_ ganzzahligen Partitionen \| \_ pow2 \| Partitionierung von \_ Bruchteil der \_ ungeraden \| \_ \_ Dezimalstellen sogar*<br/> | \[in \] der Mosaik-Partitionierung.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Aus Sicht der Hardware \_ verhält sich pow2 genauso wie eine \_ ganze Zahl. Der HLSL-Shader-Autor und/oder-Kompilier Code ist für die Rundung von Tess Factors auf die Potenzen von 2 fest.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle                 | Domain | Geometrie | Pixel | Compute |
|--------|----------------------|--------|----------|-------|---------|
|        | Deklarations Abschnitt |        |          |       |         |



 

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

 

 





