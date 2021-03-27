---
title: LOD (SM 4.1-ASM)
description: Gibt die Detailebene (LOD) zurück, die für die Textur Filterung verwendet wird.
ms.assetid: A5931203-8CD7-4FC9-A4A4-CA981F38C7A3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c1ca5a22a735945b76a60c175c665c5cf58fb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719410"
---
# <a name="lod-sm41---asm"></a>LOD (SM 4.1-ASM)

Gibt die Detailebene (LOD) zurück, die für die Textur Filterung verwendet wird.



| LOD dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource \[ . Swizzle \] , srcsampler |
|--------------------------------------------------------------------------------|



 



| Element                                                                                                               | BESCHREIBUNG                                     |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[in \] der Adresse der Ergebnisse.<br/>   |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*<br/>     | \[in \] einem Satz von Texturkoordinaten.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*<br/> | \[in \] einem Textur Register.<br/>           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*<br/>     | \[in \] einem Samplerregister.<br/>           |



 

## <a name="remarks"></a>Bemerkungen

Dies verhält sich wie die [Beispiel](sample--sm4---asm-.md) Anweisung, aber ein gefiltertes Beispiel wird nicht generiert. Die-Anweisung berechnet den folgenden Vektor ("clampedlod", "nonclampedlod", "0", 0). Nonclampedlod ist ein berechneter Lod-Wert, der eine beliebige Klammer des Samplers oder der Textur ignoriert (d. h., er kann negative Werte zurückgeben). Clampedlod ist ein berechneter Lod-Wert, der von der eigentlichen **Beispiel** Anweisung verwendet wird. Das Swizzle in *srkresource* ermöglicht es, dass die zurückgegebenen Werte willkürlich durchlaufen werden, bevor Sie in das Ziel geschrieben werden.

Wenn keine Ressource an den angegebenen Slot gebunden ist, wird 0 zurückgegeben.

Wenn der Sampler das anisotrope-Filtern verwendet, sollte die Lod dem Bruchteil der MIP-Ebene entsprechend der geringeren Achse des elliptischen Speicherplatzes entsprechen.

Dies gilt für die folgenden Textur Typen: Texture1D, Texture2D, Texture3D und texturecube.

Die **Lod** -Anweisung ist nicht definiert, wenn Sie mit einem Sampler verwendet wird, der die MIP-Filterung für Punkte angibt, insbesondere jede d3d10 \_ Filter-Enumeration, die auf dem MIP- \_ Punkt endet (Ein Beispiel hierfür wäre d3d10 \_ Filter \_ minimale \_ mag- \_ MIP- \_ Punkt.)

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





