---
title: default (sm4 - asm)
description: Eine optionale Bezeichnung in einer switch-Anweisung.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d54c3bbe83bd2499bdc2d50a30153bbc8b66e6ee53c29125b6a66416e419aa1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792676"
---
# <a name="default-sm4---asm"></a>default (sm4 - asm)

Eine optionale Bezeichnung in einer [switch-Anweisung.](switch--sm4---asm-.md)



| default |
|---------|



 

## <a name="remarks"></a>Hinweise

Diese Anweisung funktioniert wie der Standard **in** C. Das Durchfallen ist nur gültig, wenn kein Code hinzugefügt wurde, sodass mehrere Fälle (einschließlich **Standard)** denselben Codeblock gemeinsam verwenden können.

In einem **Switchkonstrukt** ist nur eine **Standard-Anweisung** zulässig.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




