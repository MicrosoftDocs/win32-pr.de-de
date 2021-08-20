---
title: else (sm4 - asm)
description: Startet einen else-Block.
ms.assetid: CFF25E78-D986-4EC5-B542-B3396EFF88E1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36f676a1a14f23923e8cebe44a0539a8ba5f382c010fc87a292e77afe1470c57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512160"
---
# <a name="else-sm4---asm"></a>else (sm4 - asm)

Startet einen **else-Block.**



| else |
|------|



 

## <a name="remarks"></a>Hinweise

Das Tokenformat enthält zur Vereinfachung den Offset der entsprechenden [endif-Anweisung](endif--sm4---asm-.md) im Shader.

Im folgenden Beispiel wird die Verwendung der **else-Anweisung** veranschaulicht.

``` syntax
                if     // any of the various forms of if* statements
                   ...
                else   // (optional)
                   ...
                endif
```

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




