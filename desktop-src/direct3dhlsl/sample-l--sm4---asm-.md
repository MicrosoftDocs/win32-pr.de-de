---
title: sample_l (sm4 – asm)
description: Stichproben von Daten aus dem angegebenen Element/der angegebenen Textur unter Verwendung der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filtermodus. | sample_l (sm4 – asm)
ms.assetid: D285F63E-1026-45F1-9959-6F5AB2A27C95
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbd65be095476cdac16ee95009994041af0b1812101b1d0d0b9a33a315ed58d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671810"
---
# <a name="sample_l-sm4---asm"></a>sample \_ l (sm4 - asm)

Stichproben von Daten aus dem angegebenen Element/der angegebenen Textur unter Verwendung der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filtermodus.



| sample \_ l \[ \_ aoffimmi(u,v,w) \] dest \[ .mask , \] srcAddress \[ .swizzle \] , srcResource \[ .swizzle \] , srcSampler, srcLOD.select \_ component |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                               | Beschreibung                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[in \] Die Adresse der Ergebnisse des Vorgangs.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[in \] Eine Gruppe von Texturkoordinaten. Weitere Informationen finden [](sample--sm4---asm-.md) Sie in der Beispielanweisung.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] einem Texturregister. Weitere Informationen finden  Sie in der Beispielanweisung.<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[in \] einem Samplerregister. Weitere Informationen finden  Sie in der Beispielanweisung.<br/>                                 |
| <span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srcLOD*<br/>                     | \[in \] der LOD.<br/>                                                                                                 |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung ist mit [der Beispielanweisung](sample--sm4---asm-.md)identisch, mit der Ausnahme, dass LOD direkt von der Anwendung als Skalarwert bereitgestellt wird, der keine Anisotropie darstellt. Diese Anweisung ist in allen progammierbaren Shaderstufen verfügbar.

**sample \_ l** samplingt die Textur mithilfe von *srcLOD* als LOD. Wenn der LOD-Wert <= 0 ist, wird die 0(größte Karte) ausgewählt, wobei der Lupenfilter angewendet wird (falls zutreffend basierend auf dem Filtermodus). Da *srcLOD* ein Gleitkommawert ist, wird der Bruchwert verwendet, um zwischen zwei Mip-Ebenen zu interpolieren, wenn der Minify-Filter LINEAR oder mit anisotroper Filterung ist.

**Sample \_ l** ignoriert Adressableitungen, sodass das Filterverhalten rein isotrop ist. Da Ableitungen ignoriert werden, verhält sich die Anisotrope Filterung als isotrope Filterung.

Sampler gibt an, dass MIPLODBIAS und MAX/MINMIPLEVEL berücksichtigt werden.

Bei Verwendung im Pixel-Shader impliziert **Sample \_ l,** dass die Wahl der LOD pro Pixel erfolgt, ohne auswirkungen auf benachbarte Pixel, z. B. im gleichen 2x2-Stempel.

Beim Abrufen aus einem Eingabeslot, an den nichts gebunden ist, wird für alle Komponenten 0 zurückgegeben.

Diese Anweisung gilt für die folgenden Shaderstufen:



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

 

 





