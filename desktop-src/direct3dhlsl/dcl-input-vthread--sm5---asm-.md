---
title: dcl_input vThread (sm5 – asm)
description: Deklarieren Sie Eingabe-IDs des Compute-Shaders.
ms.assetid: C041863A-32B0-4588-A1A9-E416AF9B723C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07c7eef8fe85ae39fb61d9e34b600805d38f7b92d5dbceb7dc2218b1515b6d36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286198"
---
# <a name="dcl_input-vthread-sm5---asm"></a>dcl \_ input vThread (sm5 – asm)

Deklarieren Sie Eingabe-IDs des Compute-Shaders.



| dcl \_ input {vThreadID.xyz\|vThreadGroupID.xyz\| vThreadIDInGroup.xyz\|vThreadIDInGroupFlattened} |
|--------------------------------------------------------------------------------------------------|



 



| Element                                                                                                                                                                                                                                                                                                                                                                          | Beschreibung                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="vThreadID___vThreadGroupID___vThreadIDInGroup___vThreadIDInGroupFlattened"></span><span id="vthreadid___vthreadgroupid___vthreadidingroup___vthreadidingroupflattened"></span><span id="VTHREADID___VTHREADGROUPID___VTHREADIDINGROUP___VTHREADIDINGROUPFLATTENED"></span>*vThreadID \| vThreadGroupID \| vThreadIDInGroup \| vThreadIDInGroupFlattened*<br/> | \[in \] Der 3-Komponenten-ID-Wert der 32-Bit-Ganzzahl ohne Vorzeichen.<br/> |



 

**dcl \_ input** ist eine vorhandene Deklaration in anderen Shaderstufen. Sie wird im Compute-Shader verwendet, um die verschiedenen 3-Komponenten-GANZZAHL-ID-Werte ohne Vorzeichen zu deklarieren, die für den Compute-Shader eindeutig sind. Sie lauten wie folgt:

-   vThreadID.xyz
-   vGroupID.xyz
-   vThreadIDInGroup.xyz
-   vThreadIDInGroupFlattened (einzelne Komponente)

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





