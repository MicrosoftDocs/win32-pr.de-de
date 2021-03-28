---
title: dcl_hs_join_phase_instance_count (SM5-ASM)
description: Deklarieren Sie die Anzahl der joinphasen-Instanzen in einer Hull-Shader-joinphase.
ms.assetid: 9951B849-0537-4D08-9ADE-8CF6FF51A193
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34c3acc7074170ab4561a54e67668698d58b7ac1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389606"
---
# <a name="dcl_hs_join_phase_instance_count-sm5---asm"></a>Anzahl der DCL \_ HS \_ \_ -joinphasen \_ Instanzen \_ (SM5-ASM)

Deklarieren Sie die Anzahl der joinphasen-Instanzen in einer Hull-Shader-joinphase.



| DCL \_ HS \_ \_ -joinphasen- \_ \_ Instanzanzahl {1... Max 32-Bit uint} |
|--------------------------------------------------------------|



 



| Element                                                   | BESCHREIBUNG                           |
|--------------------------------------------------------|---------------------------------------|
| <span id="N"></span><span id="n"></span>*Nr*<br/> | \[in \] der Instanzanzahl.<br/> |



 

## <a name="remarks"></a>Bemerkungen

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

 

 





