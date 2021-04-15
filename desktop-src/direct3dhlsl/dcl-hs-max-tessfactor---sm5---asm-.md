---
title: dcl_hs_max_tessfactor (SM5-ASM)
description: Deklarieren Sie den maxtess Factor für den Patch.
ms.assetid: 7EF0FD81-69FE-49F6-95DF-0C452A90A713
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69bd20fc8f4a3687988e8b100975f74016a45ae6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993246"
---
# <a name="dcl_hs_max_tessfactor-sm5---asm"></a>DCL \_ HS \_ Max \_ Tess Factor (SM5-ASM)

Deklarieren Sie den maxtess Factor für den Patch.



| DCL \_ HS \_ Max. Mosaik \_ Faktor n |
|----------------------------|



 



| Element                                                   | BESCHREIBUNG                          |
|--------------------------------------------------------|--------------------------------------|
| <span id="n"></span><span id="N"></span>*Nr*<br/> | \[in \] maxtess Factor.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Maxtess Factor ist ein float32-Wert im Bereich {1,0... 64,0}.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        | X    |        |          |       |         |



 

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

 

 





