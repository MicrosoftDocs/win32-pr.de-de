---
title: Standard (SM4-ASM)
description: Eine optionale Bezeichnung in einer Switch-Anweisung.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b92364212e4d20a6e9229c057ba424f43f8f8556
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976337"
---
# <a name="default-sm4---asm"></a>Standard (SM4-ASM)

Eine optionale Bezeichnung in einer [Switch](switch--sm4---asm-.md) -Anweisung.



| default |
|---------|



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung funktioniert genau wie **Standard** in C. das durchlaufen ist nur gültig, wenn kein Code hinzugefügt wurde, sodass mehrere Fälle (einschließlich **Standard**) denselben Codeblock gemeinsam verwenden können.

In einem switchkonstrukt ist **nur eine** **default** -Anweisung zulässig.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




