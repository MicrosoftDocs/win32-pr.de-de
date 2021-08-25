---
title: sample_c_lz (sm4 – asm)
description: Führt einen Vergleichsfilter aus. Diese Anweisung verhält sich wie beispiel \_ c, außer LOD ist 0, und Ableitungen werden ignoriert.
ms.assetid: 5F11F091-AF2F-4293-88C7-824F11FE01E4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b2866bdfddf91f9bd6ab1bbccbc9d76de071065b3cf28c1093cb1fdb041f3db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981500"
---
# <a name="sample_c_lz-sm4---asm"></a>sample \_ c \_ lz (sm4 - asm)

Führt einen Vergleichsfilter aus. Diese Anweisung verhält sich wie [beispiel \_ c](sample-c--sm4---asm-.md), außer LOD ist 0, und Ableitungen werden ignoriert.



| sample \_ c \_ lz \[ \_ aoffimmi(u,v,w) \] dest \[ .mask , \] srcAddress \[ .swizzle \] , srcResource.r, / must be .r swizzle srcSampler, srcReferenceValue / single component selected |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                                                       | BESCHREIBUNG                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                                            | \[in \] Die Adresse der Ergebnisse des Vorgangs.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[in \] Eine Gruppe von Texturkoordinaten. Weitere Informationen finden [](sample--sm4---asm-.md) Sie in der Beispielanweisung.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[in \] einem Texturregister. Weitere Informationen finden  Sie in der Beispielanweisung.<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[in \] einem Samplerregister. Weitere Informationen finden  Sie in der Beispielanweisung.<br/>                                 |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[in \] Ein Register mit einer einzelnen ausgewählten Komponente, die im Vergleich verwendet wird.<br/>                            |



 

## <a name="remarks"></a>Hinweise

"lz" steht für level-zero. Da Ableitungen ignoriert werden, ist diese Anweisung in anderen Shadern als dem Pixelshader verfügbar.

Wenn diese Anweisung mit einer mipmapped-Textur verwendet wird, wird LOD 0 entnommen, es sei denn, der Sampler verfügt über eine LOD-Klammer, die die LOD an anderer Stelle platziert, oder wenn ein LOD-Bias vorliegt, der einfach bei 0 beginnt. Da Ableitungen ignoriert werden, verhält sich die Anisotrope Filterung als isotrope Filterung.

In Pixel-Shadern kann diese Anweisung im Gegensatz zu **Beispiel \_ c** innerhalb der unterschiedlichen Flusssteuerung verwendet werden, wenn die Texturkoordinaten im Shader abgeleitet werden.

Beim Abrufen aus einem Eingabeslot, an den nichts gebunden ist, wird für alle Komponenten 0 zurückgegeben.

Diese Anweisung ist aus Konsistenzgründen in allen Shadern verfügbar, nicht nur im Pixelshader.



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| X             | X               | w            |



 

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

 

 





