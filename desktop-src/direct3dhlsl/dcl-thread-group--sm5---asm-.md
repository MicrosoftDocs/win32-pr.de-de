---
title: dcl_thread_group (sm5 – asm)
description: Deklarieren Sie die Threadgruppengröße.
ms.assetid: CB8192C4-100D-49B6-94E7-6CD3AEC28149
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5402e53e2252d8019ba553c6a8ff449200625b1469ee923f3c26234f1faa292e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515478"
---
# <a name="dcl_thread_group-sm5---asm"></a>dcl \_ thread \_ group (sm5 – asm)

Deklarieren Sie die Threadgruppengröße.



| dcl \_ thread \_ group x, y, z |
|----------------------------|



 



| Element                                                   | BESCHREIBUNG                                                        |
|--------------------------------------------------------|--------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Eine angepasste 32-Bit-Ganzzahl. 1 <= x <= 1024 <br/> |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[in \] Eine angepasste 32-Bit-Ganzzahl. 1 <= y <= 1024<br/>  |
| <span id="z"></span><span id="Z"></span>*Z*<br/> | \[in \] Eine angepasste 32-Bit-Ganzzahl. 1 <= z <= 64<br/>    |



 

## <a name="remarks"></a>Hinweise

x \* y \* z <= 1024

Diese Threadgruppendeklaration muss einmal in einem Compute-Shader angezeigt werden.

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

 

 





