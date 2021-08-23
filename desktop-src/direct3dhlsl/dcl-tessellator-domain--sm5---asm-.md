---
title: dcl_tessellator_domain (sm5 - asm)
description: Deklarieren Sie die Mosaikdomäne in einem Deklarationsabschnitt für den Hüllen-Shader und den Domänen-Shader.
ms.assetid: 11A1D9D0-D848-4750-875B-7060CE1CF42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52a027e9fab091cf31e8577266015e974ec78033fe19a9542f0aa3c6ca4651db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986710"
---
# <a name="dcl_tessellator_domain-sm5---asm"></a>dcl \_ tessellator \_ domain (sm5 - asm)

Deklarieren Sie die Mosaikdomäne in einem Deklarationsabschnitt für den Hüllen-Shader und den Domänen-Shader.



| dcl \_ tessellator \_ domain {domain \_ isoline \| domain \_ tri \| domain \_ quad} |
|---------------------------------------------------------------------------|



 



| Element                                                                                                                                                                                | Beschreibung                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*Domain \_ isoline \| domain tri domain \_ \| \_ quad*<br/> | \[in \] Der Domäne.<br/> |



 

## <a name="remarks"></a>Hinweise

Das Verhalten ist nicht definiert, wenn der Hüllen-Shader und der Domänen-Shader nicht übereinstimmende Domänen oder andere in Konflikt stehende Verlangsamungen bereitstellen.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf                 | Domain | Geometrie | Pixel | Compute |
|--------|----------------------|--------|----------|-------|---------|
|        | Abschnitt "Deklarationen" | X      |          |       |         |



 

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

 

 





