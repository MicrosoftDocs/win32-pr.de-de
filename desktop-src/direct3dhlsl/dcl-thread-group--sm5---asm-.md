---
title: dcl_thread_group (SM5-ASM)
description: Thread Gruppengröße deklarieren.
ms.assetid: CB8192C4-100D-49B6-94E7-6CD3AEC28149
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8141c80e82f1dfd1ae5a4d360d04fac32ba5221
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038360"
---
# <a name="dcl_thread_group-sm5---asm"></a>DCL \_ \_ -Thread Gruppe (SM5-ASM)

Thread Gruppengröße deklarieren.



| DCL- \_ Thread \_ Gruppe x, y, z |
|----------------------------|



 



| Element                                                   | BESCHREIBUNG                                                        |
|--------------------------------------------------------|--------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[in \] einer 32-Bit-Ganzzahl mit Vorzeichen. 1 <= x <= 1024 <br/> |
| <span id="y"></span><span id="Y"></span>*Teenie*<br/> | \[in \] einer 32-Bit-Ganzzahl mit Vorzeichen. 1 <= y <= 1024<br/>  |
| <span id="z"></span><span id="Z"></span>*z*<br/> | \[in \] einer 32-Bit-Ganzzahl mit Vorzeichen. 1 <= z <= 64<br/>    |



 

## <a name="remarks"></a>Bemerkungen

x \* y \* z <= 1024

Diese Thread Gruppen Deklaration muss einmal in einem Compute-Shader vorkommen.

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

 

 





