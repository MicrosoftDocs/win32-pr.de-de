---
title: dcl_input vthread (SM5-ASM)
description: Deklarieren Sie Compute-Shadereingabe-IDs.
ms.assetid: C041863A-32B0-4588-A1A9-E416AF9B723C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf6a7bb19feef95eae9cc153911407b206fde16
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719482"
---
# <a name="dcl_input-vthread-sm5---asm"></a>DCL \_ -Eingabe-vthread (SM5-ASM)

Deklarieren Sie Compute-Shadereingabe-IDs.



| DCL- \_ Eingabe {vThreadID.XYZ \|vThreadGroupID.XYZ \| vThreadIDInGroup.XYZ \|vthreadidingroupflatchten} |
|--------------------------------------------------------------------------------------------------|



 



| Element                                                                                                                                                                                                                                                                                                                                                                          | BESCHREIBUNG                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="vThreadID___vThreadGroupID___vThreadIDInGroup___vThreadIDInGroupFlattened"></span><span id="vthreadid___vthreadgroupid___vthreadidingroup___vthreadidingroupflattened"></span><span id="VTHREADID___VTHREADGROUPID___VTHREADIDINGROUP___VTHREADIDINGROUPFLATTENED"></span>*vthreadid \| vthreadgroupid \| vthreadidingroup \| vthreadidingroupflatchten*<br/> | \[im \] 32-Bit-Ganzzahl-ID-Wert ohne Vorzeichen.<br/> |



 

die **DCL- \_ Eingabe** ist eine vorhandene Deklaration in anderen Shader-Stufen. Es wird im COMPUTE-Shader verwendet, um die verschiedenen ganzzahligen, ganzzahligen 32-Bit-ID-Werte mit drei Komponenten für den Compute-Shader zu deklarieren. Sie lauten wie folgt:

-   vThreadID.xyz
-   vGroupID.xyz
-   vThreadIDInGroup.xyz
-   vthreadidingroupflatchten (einzelne Komponente)

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

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

 

 





