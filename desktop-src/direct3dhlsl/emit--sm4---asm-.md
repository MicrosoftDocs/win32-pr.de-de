---
title: Ausgabe (SM4-ASM)
description: Gibt einen Scheitelpunkt aus.
ms.assetid: FDD18CCD-8088-46BD-897C-434B77FF81E6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b17711b6f9cf5d707fb8eae3465100a78620c0c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719356"
---
# <a name="emit-sm4---asm"></a>Ausgabe (SM4-ASM)

Gibt einen Scheitelpunkt aus.



| ausgeben |
|------|



 

## <a name="remarks"></a>Bemerkungen

die **Ausgabe bewirkt,** dass alle deklarierten o- \# Register aus dem Geometry-Shader ausgelesen werden, um einen Scheitelpunkt zu generieren.

Wenn mehrere **Ausgabe** Aufrufe ausgegeben werden, werden primitive generiert.

die **Ausgabe kann beliebig** oft in einem Geometry-Shader vorkommen, einschließlich innerhalb der Fluss Steuerung.

Wenn Streams deklariert wurden, müssen Sie den [ \_ Ausgabestream](emit-stream--sm5---asm-.md)verwenden.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
|               | x               |              |



 

### <a name="minimum-shader-model"></a>Minimaler Shader-Modell

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

 

 




