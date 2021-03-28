---
title: sample_c_lz (SM4-ASM)
description: Führt einen Vergleichs Filter aus. Diese Anweisung verhält sich wie Beispiel \_ c, mit dem Unterschied, dass Lod 0 ist und Ableitungen ignoriert werden.
ms.assetid: 5F11F091-AF2F-4293-88C7-824F11FE01E4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24ec2889dd3ea4c86af51c8e36bf2e302c6ad4dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389530"
---
# <a name="sample_c_lz-sm4---asm"></a>Beispiel \_ c \_ LZ (SM4-ASM)

Führt einen Vergleichs Filter aus. Diese Anweisung verhält sich wie [Beispiel \_ c](sample-c--sm4---asm-.md), mit dem Unterschied, dass Lod 0 ist und Ableitungen ignoriert werden.



| Beispiel \_ c \_ LZ \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource. r,//muss lauten. r Swizzle srcsampler, srkreferencevalue//Single Component Selected |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                                                       | BESCHREIBUNG                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                            | \[in \] der Adresse der Ergebnisse des Vorgangs.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*<br/>                             | \[in \] einem Satz von Texturkoordinaten. Weitere Informationen finden Sie in der [Beispiel](sample--sm4---asm-.md) Anweisung.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*<br/>                         | \[in \] einem Textur Register. Weitere Informationen finden Sie in der **Beispiel** Anweisung.<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*<br/>                             | \[in \] einem Samplerregister. Weitere Informationen finden Sie in der **Beispiel** Anweisung.<br/>                                 |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srkreferencevalue*<br/> | \[in \] einem Register, bei dem eine einzelne Komponente ausgewählt ist, die im Vergleich verwendet wird.<br/>                            |



 

## <a name="remarks"></a>Bemerkungen

Die "LZ" steht für die Ebene 0 (null). Da Ableitungen ignoriert werden, ist diese Anweisung in anderen Shadern als dem Pixelshader verfügbar.

Wenn diese Anweisung mit einer Mipmapping-Textur verwendet wird, wird Lod 0 als Stichprobe verwendet, es sei denn, der Sampler verfügt über eine Lod-Klammer, bei der die Lod an anderer Stelle platziert wird Da Ableitungen ignoriert werden, verhält sich die anisotrope Filterung als isotrope Filter.

In Pixel-Shadern kann diese Anweisung in einer unterschiedlichen Fluss Steuerung verwendet werden, wenn die Texturkoordinaten im Shader abgeleitet sind, im Gegensatz zum **Beispiel \_ c**.

Wenn Sie aus einem Eingabe Slot abrufen, an das nichts gebunden ist, wird 0 für alle Komponenten zurückgegeben.

Diese Anweisung ist aus Gründen der Konsistenz in allen Shadern, nicht nur dem Pixelshader, verfügbar.



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| X             | X               | w            |



 

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

 

 





