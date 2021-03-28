---
title: dcl_tessellator_domain (SM5-ASM)
description: Deklarieren Sie die Domäne für den Mosaik Prozess in einem Hull-Shader-Deklarations Abschnitt und dem Domänen-Shader.
ms.assetid: 11A1D9D0-D848-4750-875B-7060CE1CF42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8724ee9564239ffaca6f5c34a39fb1b4ef967e51
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389591"
---
# <a name="dcl_tessellator_domain-sm5---asm"></a>DCL \_ \_ -Mosaik Domäne (SM5-ASM)

Deklarieren Sie die Domäne für den Mosaik Prozess in einem Hull-Shader-Deklarations Abschnitt und dem Domänen-Shader.



| DCL-Mosaik \_ \_ Domäne {Domänen \_ Isolat \| Domäne \_ Tri \| Domäne \_ Quad} |
|---------------------------------------------------------------------------|



 



| Element                                                                                                                                                                                | BESCHREIBUNG                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*Domäne \_ isolin \| Domäne \_ Tri \| Domäne \_ Quad*<br/> | \[in \] der Domäne.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das Verhalten ist nicht definiert, wenn der Hull-Shader und der Domänen-Shader nicht übereinstimmende Domänen oder andere widersprüchliche Abweichungen bereitstellen.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle                 | Domain | Geometrie | Pixel | Compute |
|--------|----------------------|--------|----------|-------|---------|
|        | Deklarations Abschnitt | X      |          |       |         |



 

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

 

 





